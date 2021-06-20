# pc-auto-brightness

Android application which transmits brightness data to a PC listener using UDP which then used to change the brightness of the PC screen automatically.

> ## Install

Clone this repo using the command 

    git clone https://github.com/akhileshkoti/pc-auto-brightness.git

or download the **[zip file](https://github.com/akhileshkoti/pc-auto-brightness/archive/refs/heads/master.zip)**.

> ## Usage

### Dependencies

  Navigate to udp_listener directory and Install the python dependencies using the command

    pip install -r requirements.txt

### Setting up the UDP Listener

  Navigate to udp_listener directory and set up the listener using the following commands

- #### To run as a background process

        pythonw script.pyw

- #### To debug the listener 

    Open the script.py file in an editor or use the command
        
        python script.py

- #### To run the listener as a startup process

    Create a shortcut for startup.bat file and copy it to the startup file in Windows.
  
    To do this 
    - Open Run dialog box, enter the following command and press OK
        
            shell:startup
      
      Now copy the startup.bat shortcut into that folder
    
    or
  
    - Navigate to the following location and paste the shortcut of startup.bat in that location
  
            C:\Users\[User_Name]\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup


 ### Setting up the UDP Broadcast in the android

  - Download and Install the Broadcast.apk in your android from the **[repo](https://github.com/akhileshkoti/pc-auto-brightness)**.

  - Enter the host ip address as the private ip address of your udp_listener(pc).
  
    :warning: Both your listener and broadcasting devices should be on the same network
   
    To know the ip address of the pc go to command prompt and enter the following command and hit enter
   
        ipconfig
        
  - Enter the Port value as **1201** since it the same port the listener is bound to.

  - Press **CONNECT** to start the broadcast.

  - This sends the data to the listener which changes the brightness of the pc automatically.

  - To stop the broadcast press **STOP** in the app.

  - This stops the broadcast and the pc brightness is maintained at the same level until the broadcast is started again or brightness is manually changed.
  
  
  # Contributors
  
  :man_technologist: **[Ronin](https://github.com/raja-ravi-prakash)**
    
  :man_technologist: **[akhil](https://github.com/akhileshkoti)**
  
  
