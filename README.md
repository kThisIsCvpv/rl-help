# RuneLite Plugin Compilation (for Noobs)
This guide was made by Yuri-chan. A more advanced guide can be found on the [official RuneLite page](https://github.com/runelite/runelite/wiki/Building-with-IntelliJ-IDEA).

## Required Software List:
### Java JDK 8 or higher
Download: https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

File Size: Approximately 200.0~ MB

![alt text](https://www.kthisiscvpv.com/X9wLm1555022461ec3PU.png "Java 8 Download")

Note: Java JRE **will not** work. Java JRE is commonly used by consumers products. Java JDK contains libraries required by developer programs. Building with IntelliJ, the compilation software below, requires the Java JDK 8 software. You can have multiple Java versions on your PC without confliction.

---

### Git
Download: https://git-scm.com/downloads

File Size: Approximately 40.0~ MB

![alt text](https://www.kthisiscvpv.com/Eivby1555022607jq7bM.png "Git Download")

---

### IntelliJ IDEA Community Edition
Download https://www.jetbrains.com/idea/download/#section=windows

File Size: Approximately 480.0~ MB
![alt text](https://www.kthisiscvpv.com/lVMg015550228076zQbW.png "IntelliJ Download")

## Software Installation Process

Please install the programs listed in the requirements above **in the order** that they are listed. In every installation process, you are able to just spam on the **[NEXT]** and **[FINISH]** buttons. There is no ad-ware lurking in these development tools; and hopefully never will.

## RuneLite Installation Process

At this point, you should have all 3 of the required software installed. This section begins the tutorial on how to build RuneLite from scratch using the compiler. 

#### 1. Launch IntelliJ Idea
Simple right? I hope you don't get stuck here...
#### 2. Downloading RuneLite Source
Click on `Check out from Version Control` and then select `Git`.

![alt text](https://www.kthisiscvpv.com/uccXt1555024283Onx5R.png "Git Checkout")

When asked for the repository location, enter `https://github.com/runelite/runelite` as the URL. Then click `Clone`.

![alt text](https://www.kthisiscvpv.com/IQ8vO1555024443MKzm8.png "Git Clone")

When you are prompted to import the project, hit `Yes`.

![alt text](https://www.kthisiscvpv.com/XwvuB15550245131mGLg.png "Checkout Prompt")

Import the project as `Import project from external model > Maven > Next ...`
_Note: You might not be given this window. It is perfectly fine; IntelliJ has already correctly imported it for you._

![alt text](https://www.kthisiscvpv.com/eCRtZ1555024570b6NhZ.png "Import Project")

#### 3. Installing Lombok

Your screen should currently look something like this.

![alt text](https://www.kthisiscvpv.com/vs1A41555024883LNQIe.png "Current Screen")

Press `Alt + 1` on your keyboard to bring up the sidebar menu. Navigate to `File > Settings`.

![alt text](https://www.kthisiscvpv.com/m0eTy1555025029yhiMr.png "Configure Settings")

Navigate to `Plugins > Search` and search for `Lombok`. Install this software as it is used to compile RuneLite.

![alt text](https://www.kthisiscvpv.com/bXcPm15550251085zFLm.png "Search Lombok")

At this point, you will be prompted to restart your IDE. You should do so.

#### 4. Installing RuneLite

In the top right corner of your screen find a dropdown box click it and navigate to `Edit Configurations...`.

![alt text](https://www.kthisiscvpv.com/FwHCC1555025744fulpq.png "Edit Configurations")

Add a new Maven configuration by clicking `[+] > Maven`.

![alt text](https://www.kthisiscvpv.com/eMxht1555025761eXyub.png "Adding Maven")

Click the folder next to `Working Directory` and select `runelite-parent`.

![alt text](https://www.kthisiscvpv.com/uO1qx1555025942OGbNy.png "Select Directory")

The under `Command line`, enter `install -DskipTests -U`. You can now hit `Apply` and `Okay` to close the window.

![alt text](https://www.kthisiscvpv.com/M85WO1555026099piRGJ.png "Apply Configurations")

Back to where the `Edit Configurations...` was, you should now see a `M` option. Click the `Play` button next to it. 
_Note: If your button isn't green, you might need to wait a couple minutes for your IntelliJ to finish indexing the files._

![alt text](https://www.kthisiscvpv.com/3wsVD1555026365FZvV8.png "Run Maven")

A console will now appear at the bottom of the screen. Wait until the console shows an exit code before continuing. 

![alt text](https://www.kthisiscvpv.com/X0Kkr1555026572rvRFo.png "Exit Code")
