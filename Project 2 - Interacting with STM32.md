*** Part 1: Solo Setup ***
1. Set up your environment: CubeIDE and CubeProgrammer
	1. Download the CubeIDE (includes CubeMX) from the [ST website](https://www.st.com/en/development-tools/stm32cubeide.html)
		1. Find the installer that matches your operating system
		2. I'd recommend downloading the latest version (1.19.0 at the time of writing) using the pink "Get latest" button
		3. Once you click "Get latest", you will be prompted to either create an ST microelectronics account or continue as guest.
			- You will have to make a myST account for step 2: downloading SDK, so it might be easier to to create an account now.
		4. Enter your SDSU email or another email you can access to download the IDE using the link they send you. It is only valid for 24 hours.
		5. Navigate to your email, click "Download Now" and it will start to download a zip file
		6. Extract the zip file and open the .exe application
		7. Go through the installation wizard
	2. Download STM32CubeProgrammer (used to flash code to board using ST-Link) from the [ST Website](https://www.st.com/en/development-tools/stm32cubeprog.html)
		1. Similar process to downloading CubeIDE in previous step (pink button to get latest, sign in as guest, email link)
		2. Latest version as of writing is 2.20.0
		3. Extract zip file and open the application
		4. After installing cube programmer, another window should pop up called "Device Driver Intallation Wizard". This is to download the ST-Link USB driver. Mac and Linux OS are supposed to natively support and may not need this driver. But unless there are any issues with installing this driver, you don't have to do anything. Later on, if the Device Manager shows "unknown ST-Link" you may need to reinstall the driver
	3. NOTES:
		- You will need around 5GB of free space on your personal laptop to install these tools (sorry) especially because of the zip files. But after installing Cube IDE and Cube Programmer, you can delete the zip file and exracted folder again ONLY AFTER INSTALLATION IS COMPLETE to save space!
		- These tools sometimes take a while to open after doing the setup wizard, especially Cube IDE. It will also show a pop up that asks something like "do you want to exclude from Windows defender scans for faster startup?" which you can do if you're comfortable. Essentially, don't panic if things take a while.

2. Verify IDE and SDK (software development kit)
	1. Open STM32CubeIDE
	2. Go to top toolbar: Help -> Configuration Tool -> Manage Embedded Software Packages
	3. Once the Embedded Software Packages Manager opens, click the dropdown for STM32F0 (should be second on the list) and check the box for the most recent (1.11.5 at time of writing) release of "STM32Cube MCU Package for STM32F0 Series"
	4. Click install
	5. Sign into the myST account you created, or register f you have not. If the link to create account within the package manager window doesn't work, exit out of it, go to Help -> STM32 Cube Updates -> Connection to myST. Click the button that says "Enter myST account information" or similar and login
	6. After signing in, open the Manage Embedded Software Packages window again if it closed (repeat steps 2-4)
	7. Verify download of SDK: in your file explorer, verify the directory C:\Users\youruser\STM32Cube\Repository\STM32Cube_FW_F0_V1.11.5 (or UNIX equivalent) which is where the example code is installed
	9. Open example code:
		1. In the toolbar, go to File -> Open Projects from File System
		2. Click the "Directory" button and navigate to the above path that you just checked within your C drive. Then, click through Repository -> STM32Cube_FW_F0_V1.11.5 -> STM32F042K6-Nucleo -> Examples -> GPIO -> GPIO_IOToggle
		3. Accept the popup that asks for conversion to STM32CubeIDE project
		4. Take a look through the files in this project folder, including the readme, source code, and pinout & clock configuration.
		5. Try changing the code to have the LED blink with a 1Hz frequency.

3. Create your own project
	1. File -> New -> STM32 Project
	2. In "Board Selecter", search NUCLEO-F042K6 and click "Next" after selecting it
	3. Accept default initialization of peripherals
	4. Go to Pinout & Cnfiguration tab. Confirm that LD3 is mapped to GPIO_Output/PB3

*** The following steps are intended to be tested with a Nucleo board in person ***
4. Connect the STM32 Nucleo F042K6 board to your computer with USB-C to Micro B cable. Observe the following:
	- Small LED opposite micro-B connection glows red. This is LD2, and indicates power to the board when it is on.
	- A larger LED next to the micro-B port glows red. This is LD1, and represents COM activity, aka communication to your computer.
	- Small LED labeled LD3 blinks green. This just means the board has demo code that blinks this LED, so don't worry if it doesn't blink (you might be using the test Nucleo with different code). Note: LD3 is the only user-controlled LED on the Nucleo. It is controlled by a logic level high (3.3V) on pin D13/PB3. Try locating pin D13 by looking at the board.
	- If the communication and power LEDs are not both on:
		1. Try a different USB to Micro-B cable
		2. Try connecting to another USB port on your computer
		3. Last resort: if the specific Nucleo board has already been verified to work, reintsall the ST-LINK driver (especially if you are Windows)

*** Known Issues: ***
- so far, Cube IDE has been regularly freezing and doesn't respond to commands... there are other options for interfacing with STM32 boards (like VScode's PlatformIO extension) and we want to hear member feedback before doing a standardized switch