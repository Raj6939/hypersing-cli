# hypersing-cli
Contains documentation of hypersign-cli

**Pre-requisite**
- Docker Desktop



**Install Docker Desktop for Ubuntu**

If you want to run docker locally then you need a docker desktop, go to the below link and follow the instructions.

Go to the Docker Desktop link here ```https://docs.docker.com/desktop/install/ubuntu/```

Click on the DEB Package Button to download the Debian package

![Screenshot from 2023-11-30 14-43-41](https://github.com/Raj6939/hypersing-cli/assets/67961128/eb837c27-fa0d-4aec-b07c-af1964720d2c)


After Downloading the above package, locate it in your system. In my case, it is downloaded in the Downloads Folder

![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/a1241977-d7a1-4d22-a428-436ffd7ae53a)


Then Type this command to install the downloaded Debian Package with package name

```sudo dpkg -i docker-desktop-4.25.2-amd64.deb```

![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/b8f06412-a650-4073-b6ec-69fbe08ab990)

After Installing you will see the docker desktop icon in your menu bar

![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/ac4b1784-ce4f-487c-9608-79932e7d6e1b)

Open the Docker Desktop, you can continue without signing in, finally, you will see the screen like below

![Screenshot from 2023-11-30 15-21-27](https://github.com/Raj6939/hypersing-cli/assets/67961128/fda6927d-8480-49ba-a3ff-deb1a58077f2)

Now your Docker Desktop setup is completed, do not close, minimize this window.


Now lets setup Hypersign SSI CLI

**Install hypersign-cli**

So you can install the hypersign-cli in any of one way below
  1. By Downloading Binary and then installing it using Debian package manager
      1. Download this binary by clicking this link
         
         https://github.com/hypersign-protocol/hypersign-cli/releases/download/v0.1.6/hypersign-ssi_0.1.6.daee75f-1_amd64.deb

         ![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/96539a89-f47b-4d76-94fc-96b37373da0b)

         
         If your debian file downloaded in ```Downloads``` folder then navigate there by typing ```cd```

         
      3. Locate this downloaded debian file in your machine and install it using Debian Package Manager(dkpg) by below command
         
         ```sudo dpkg -i hypersign-ssi_0.1.6.daee75f-1_amd64.deb```

         ![Screenshot from 2023-12-01 11-55-33](https://github.com/Raj6939/hypersing-cli/assets/67961128/90c91476-24d3-4bf5-be4a-6f92e1266f8e)


      4. Check if ```hypersign-ssi Cli``` is installed by typing the below command
         
         ```hypersign-cli```
         
         ![Screenshot from 2023-12-01 11-56-17](https://github.com/Raj6939/hypersing-cli/assets/67961128/7b685f17-54e3-4f65-a93c-17d3cb332bc7)

         Now you have successfully installed ```hypersign-ssi Cli```

         You can also find the necessary commands in for further setup
         
         Here are some hypersign-ssi commands with description
         
         COMMANDS
         
          ```hypersign-ssi clean```   => Stop and Delete Hypersign SSI Infrastructure configurations and data
         
          ```hypersign-ssi help```    => Display help for hypersign-ssi.
         
          ```hypersign-ssi plugins``` => List installed plugins.
         
          ```hypersign-ssi setup```   => Setup configurations for Hypersign SSI Infrastructure
         
          ```hypersign-ssi start```   => Start Hypersign SSI Infrastructure
         
          ```hypersign-ssi stop```    => Stop Hypersign SSI Infrastructure
         

     Now, you can start the setup to run the docker

     You need to first set up the hypersign-ssi cli, follow the below instructions to setup
     
     1. Type this command in your terminal
      
       ```hypersign-ssi setup```

       You will be asked to continue with Y/N. Type ```y``` and hit enter key

       ![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/1e8f013c-3a92-4b2e-b7df-8d875f0a1c24)

       Now you will get the below services for setup. You can select any service you want.
       
       ![Screenshot from 2023-12-01 12-50-28](https://github.com/Raj6939/hypersing-cli/assets/67961128/f2c65269-c4d9-402e-b0ad-00c4aecafff8)

       For this demo, we will use ```Entity Developer Dashboard``` and ```Entity API Service```

       You can select the options by pressing Space Key on your keyboard.

       ![Screenshot from 2023-12-01 12-50-39](https://github.com/Raj6939/hypersing-cli/assets/67961128/1f04c6fc-44d3-4441-b73a-2bed5808719c)

       Once the options are selected, press Enter Key. The setup will start for the selected configuration

       ![Screenshot from 2023-12-01 12-51-22](https://github.com/Raj6939/hypersing-cli/assets/67961128/3bb5852e-fdba-4ec3-bd57-5083aa0f60ce)


       **Note: Keep the Docker Desktop Open and watch what happening in the Images Section**

       Once the setup completes, you will see below screen

       ![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/7f6b1d60-181b-46c2-83a0-5086fdbd65f7)

       Your Docker Desktop Images section will look like this

       ![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/a48f97cd-2347-48cf-9abd-bceb2c53ff6a)


       Now it's time to Start (run the docker)

       To start you need to run below hypersign-ssi command

       ```hypersign-ssi start```

       You will see below output

       ![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/8e787417-b148-48c0-9ae3-e06b3794f40f)

       You can also check the Containers section, to see which images are running. The Green boxes indicate that the image is running.

       ![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/f4f1f244-1486-4830-9373-ceb333ec4b00)

       Now, Its all good to go for try,

       ![Screenshot from 2023-12-01 13-09-45](https://github.com/Raj6939/hypersing-cli/assets/67961128/18ad4c50-7b1a-4290-9625-71a75177fac7)

       Navigate to ```http://localhost:9001/``` to see Entity Developer Dashboard

       ![image](https://github.com/Raj6939/hypersing-cli/assets/67961128/bf4f8544-3e74-438f-8ad7-c50277c81b68)

       Navigate to ```http://localhost:3002/``` to see Entity Developer Dashboard Service

       




     
        




     



     

     

     

     

     




