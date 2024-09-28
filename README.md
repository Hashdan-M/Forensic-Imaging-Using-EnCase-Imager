<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/19e3c5a2044d18389e452d4a41579135e9776179/EnCase/logo.png"/></a>
<h1>Forensic Imaging Using EnCase Imager</h1>

<h2>Overview</h2>
In digital forensics, the process of collecting data from a hard drive is known as creating an image or a forensic image, especially when part of an investigation. One of the critical steps in digital forensics is generating this forensic image. However, to utilize the imaged disk, the hard drive must be appropriately set up. This means that the disk image files need to be opened and restored onto the drive using specialized imaging software; simply copying the disk image files onto the drive will not allow for recovery.
<br />
<br />
Multiple disk images can be stored on a single hard drive, and larger flash drives can also serve this purpose. The forensic image is crucial for maintaining the integrity of the evidence and ensuring that it has not been altered. Therefore, it's often necessary to verify the integrity of this image.
<br />
<br />
This article outlines the process of creating a forensic image of the digital evidence, which can then be restored to another drive. By working with a forensic image instead of the original evidence, we preserve the integrity and authenticity of the data, which can be validated using hash values. This method is also useful for safely backing up data.
<br />
<br />
While the EnCase Imager is widely recognized for its imaging capabilities and ability to preview data, it also offers a range of features that assist forensic investigators in addressing various challenges during the examination of digital devices. Let’s delve into the options that EnCase Imager offers.

<h2>Creating the Forensic Image</h2>
 
#### 1. **Launch EnCase Imager**

Open EnCase Imager and select the "**Add Local Device**" option.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/077ef46fef7ed31d52e524eeea3b1416f7c43f86/EnCase/1-1.PNG"/></a>

#### 2. **Configure Device Options**

In the menu, check all relevant options, ensuring "**Only Show Write-blocked**" is unchecked, then click "**Next**".

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/19e3c5a2044d18389e452d4a41579135e9776179/EnCase/1-2.PNG"/></a>

#### 3. Select Evidence Source

You will see a list of physical drives, logical partitions, CD-ROMs, RAM, and processes. It is best practice to choose the physical drive, as it provides a complete disk image. If necessary, you may select only specific logical drives or RAM. In this example, we will image the J drive, which is a USB drive. Check the box next to the evidence you wish to image and click "**Finish**". 

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/19e3c5a2044d18389e452d4a41579135e9776179/EnCase/1-3.PNG"/></a>

#### 4. Review Evidence Contents

The selected evidence will be listed in the interface. Double-click the evidence to view its contents. At this stage, you can choose to exclude certain files or folders from the imaging process.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/19e3c5a2044d18389e452d4a41579135e9776179/EnCase/1-4.PNG"/></a>

#### 5. Start Acquisition

Click "**Acquire**" to begin the imaging process. Enter the case details, including the case number, output path, and the file format for the image. The recommended format is E01, as it is widely supported by other forensic tools. 

*Note: It is advisable to save the image on an external drive to avoid storage issues; for practical reasons in this demonstration we will save it to in our desktop at “**C:\Users.....\Desktop\Evidence Image\1.E01.**”*

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-5.PNG"/></a>

If desired, you can also password protect and encrypt the image at this point.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-6.PNG"/></a>

#### 6. Monitor Progress

Click "**OK**" to start the acquisition process. You can monitor the progress and estimated time remaining at the bottom right of the window.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-7.PNG"/></a>

#### 7. Completion and Hash Generation

After the imaging process is complete, the image will be saved in the designated output folder.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-8.PNG"/></a>

To ensure the integrity of the evidence, generate a hash value by selecting the evidence and clicking on "**Hash**".

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-9.png"/></a>

Once hashing is done, access the report section at the bottom pane.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-10.PNG"/></a>

Right-click to copy the report and paste it into a Word or text document.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-11.png"/></a>

Save this report along with the E01 file, as it contains critical details, including hash values.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/8a1785b86524e2db74b7597d82211451c65beb0b/EnCase/1-12.PNG"/></a>

<h1>Restoring the Evidence Image</h1>

With the imaging process completed, you can now restore the acquired image to a drive.

#### 1. Open EnCase Imager

Launch EnCase Imager again and click on "**Add Evidence File**" to add the E01 image to your case.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-13.PNG"/></a>

#### 2. Select Image for Restoration

Browse to the saved image file and add it to the case. The added evidence will be displayed.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-14.PNG"/></a>

#### 3. Choose Files for Restoration

Double-click the image, select the files you wish to restore, and then select the "**Restore**" option under the "**Device**" menu.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-15.png"/></a>

#### 4. Select Target Drive

Connect the drive where you intend to restore the image and click "**Next**". All available drives will be displayed. Choose a blank drive for restoration, as existing data will be erased. In our example we will use the F Drive as the target drive.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-16.PNG"/></a>

#### 5. Verify Hash Values and Confirmation to Wipe Drive

If needed, verify the hash values and proceed by clicking "**Finish**". Type "**Yes**" in the text box to confirm that you want to wipe the existing data on the selected drive, and then click "**OK**" to begin the restoration process.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-17.PNG"/></a>

#### 6. Monitor Restoration Progress

The restoration will commence, and you can check the progress in the lower right corner of the window.

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-18.PNG"/></a>

#### 7. Completion of Restoration

Once the restoration is complete, access the target drive to verify the restored data. 

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-19.PNG"/></a>

#### 8. Data Verification

To confirm data integrity, check the report section at the bottom pane to compare hash values with those from the original image report. 

<img src="https://github.com/Hashdan-M/Forensic-Imaging-Using-EnCase-Imager/blob/f7e69d5a11131f5eeb4b81aeb843c97d3789c6ba/EnCase/1-20.PNG"/></a>

If needed, copy and save the restoration report for future reference.

<h1>Summary</h1>

By following these steps, the forensic imaging and restoration process using EnCase Imager can be effectively completed, ensuring the preservation and integrity of critical digital evidence.
