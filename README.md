
<h1> How to Use Diskpart to Repair a Corrupted Removable Drive </h1>


<h2>Project</h2>

If your USB drive or external hard drive isn’t working correctly, you can use Diskpart, a command-line tool, to repair it. Follow the steps below to clean, format, and restore your drive using Diskpart.

⚠️Important: This process will erase all data on the drive. Make sure to back up any important files before proceeding.⚠️


<h2>Utilities Used</h2>

- <b>USB Drive, Diskpart</b> 


<h2>Environments Used </h2>

- <b>Windows 11</b>

<h2>Walk-through:</h2>

First thing is to connect the removable drive, then run diskpart.
Step 1: Open run

1. Press Win + R, type diskpart, and press Enter.
   ![1](https://github.com/user-attachments/assets/475253e6-d5d1-42a5-a812-6a50997870a1)

2. Now that diskpart is running, type "list disk" to show all connected drives.
   ![2](https://github.com/user-attachments/assets/c30270c2-09c3-4125-a83a-5c1dedca0e2d)

3. Select the target disk by typing "select disk X" replacing X with the disk number of your removable drive and press Enter.
   ![3](https://github.com/user-attachments/assets/2dca86a7-2f83-41be-8867-c4820007ea72)

4. With the target disk selected, type "clean" and press Enter. ⚠️This will erase everything on your drive.
   ![4](https://github.com/user-attachments/assets/1e1ddec2-7f77-49a5-a8ce-980972b509c0)

5. Now that the drive has been wiped, a new partition has to be created. Type "create partition primary".
   ![5](https://github.com/user-attachments/assets/d4c1f142-c217-4a85-9ebc-6452505628b3)

6. The drive has to be formatted before use. I chose to use exfat in my demonstration, since it is compatible on multiple OS.
   Type format fs=exfax quick. Or replace the exfat with a format of your choice.
   ![6](https://github.com/user-attachments/assets/57accd81-8045-4c3f-a8bc-75767ac11684)

7. A window should open showing the drive is in working order and ready for use.
   ![7](https://github.com/user-attachments/assets/59386e38-b1ef-4549-866d-cf5f9a17abd7)

* Alternatively you can also open diskpart by using command prompt "cmd" if the original method does not work. To run cmd press Win + R, type cmd, and press Enter.
  Run Command Prompt as an Administrator by right-clicking and selecting “Run as administrator.” Type diskpart and press Enter, that should open up diskpart. 




