---
title: "Creating a forensic image with FTK imager"
layout: post
---

In this project, I create a forensic image with FTK imager. 

### Technologies Used: 
 
* Windows Registry
* FTK Imager

### What is a forensic image? 

A forensic image is a bit for bit copy from a source to a destination. In this context, a forensic image is a file with an associated extension type specific to forensic images.

It can represent any source media (hard drive, USB, RAM). It can also be an individual file or encompass the entirety of a device, including the whole computer or a mobile device. Essentially, it condenses everything within that device into a single image.

### What is included in a forensic image?

A forensic image includes everything, including your files and even deleted files in many instances. It also accounts for file slack, which is the remaining space where a file is stored if it doesn't perfectly fit into the defined sector of the hard drive. This leftover space can potentially contain valuable data.

Moreover, partitions created within a hard drive or volume may have what is known as partition slack—additional leftover space within that partition that could also harbour useful data.

![title](/pics/certificate-server/writeblocker1.png)

### Write blocker

Prior to initiating the forensic image, it's important to ensure that your write blocker is connected to the source device. In this particular example, I don't have a physical hardware write blocker so I use a software write blocker instead.

### USB devices

Retroactively applying the write blocker won't work if the USBs are already connected. Thus they must be detached first. In this demonstration, I have two devices—one on the E drive and one on the G drive. For the purpose of this video, the E drive will serve as the source of our forensic image.

### Introduction to FTK imager

Open FTK Imager, accessible via the ‘create disk image’ icon or the file menu. Identify the physical USB drive connected as the source for the image.

Choose the physical drive option over logical drives for comprehensive data capture and add the image destination, providing details such as case number, date, and unique descriptors.

![title](/pics/certificate-server/writeblocker1.png)

Choose the E01 image type, commonly used in forensic toolkits like Encase. Specify the case number, date, and evidence number for proper documentation. Add a unique description for reference, including details like device make, brand, and serial number.

![title](/pics/certificate-server/writeblocker1.png)

Next, assign the destination for the forensic image, ensuring it has enough space compared to the source.

Name the image file and select appropriate file fragment size (e.g., E01 for a one-gigabyte device).

Check the ‘verify images after they are created’ option for hash value verification. Run the imaging process, allowing FTK Imager to create a complete copy of the source media.

After completion, review the verification results to ensure the hash values match, confirming the integrity of the forensic image.

![title](/pics/certificate-server/writeblocker1.png)

Validate the forensic tool by considering a secondary tool to image the same source media and confirm no damage data blocks within the USB through the bad blocks list. The forensic image is now ready for further analysis using forensic tools in subsequent steps.
