# RuneLite Plugin Compilation (for Noobs)
This guide was made by Yuri-chan. A more advanced guide can be found on the [official RuneLite page](https://github.com/runelite/runelite/wiki/Building-with-IntelliJ-IDEA). This guide is for people who have never developed before and will probably have no idea what they're doing. It's filled with a bunch of pictures UwU.

## Required Software List:
### Java JDK 8 or higher
Download: https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

If it asks you to make an Oracle account, use this mirror instead. The link above might be outdated.
Mirror: http://kthisiscvpv.com/jdk-8u211-windows-x64.exe

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

Your screen should now look something like this.

![alt text](https://www.kthisiscvpv.com/vs1A41555024883LNQIe.png "Current Screen")

Go to `File > Close Project`.

![alt text](https://www.kthisiscvpv.com/uHCRu1555028780lY10h.png "Current Screen")

Re-import the project again. This time, use the `Import Project` feature.

![alt text](https://www.kthisiscvpv.com/y7cRD1555028964RIiCt.png "Import Project")

Under `File Location` enter in the location of your RuneLite. By default, it should be `~/IdeaProjects/runelite` as shown below.

![alt text](https://www.kthisiscvpv.com/MOpXz15550289923C8P9.png "Find Location")

Import the project as `Import project from external model > Maven > Next ...`

![alt text](https://www.kthisiscvpv.com/eCRtZ1555024570b6NhZ.png "Import as Maven")

#### 3. Installing Lombok

You should be back to the screen you were at before you closed your project above. Navigate to `File > Settings`.

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

A console will now appear at the bottom of the screen. Wait until the console shows an exit code before continuing. This process will take a while if you are running it for your first time.

![alt text](https://www.kthisiscvpv.com/X0Kkr1555026572rvRFo.png "Exit Code")

#### 5. Running RuneLite

You should now be able to run RuneLite. Open the File Explorer by clicking project on the left-most sidebar. Navigate to `runelite > runelite-client > src > main > java > net > runelite > client`. This is done by expanding your project workspace to the left.

![alt text](https://www.kthisiscvpv.com/OINqU1555026898VGRI4.png "Expanding Project Workspace")

Scroll down until you see the RuneLite class. Right click it and click `Run 'RuneLite.main()'` 

![alt text](https://www.kthisiscvpv.com/v6ibX1555026976yVWch.png "Run RuneLite")

RuneLite should now launch. When you launch RuneLite for the first time using this method, **the client may fail to load** and get stuck on `Fetching Game Updates 99%`, black screen,  or whatever. If this happens, re-run your Maven module back in Step 4. You may need to re-select the drop-down menu, as shown in the image below. Also, when you launch RuneLite for the first time, there may be a short wait time. This is normal.

![alt text](https://www.kthisiscvpv.com/oL5FQ1555027179LoLeW.png "Select Maven")

#### 6. Success

If you are able to get RuneLite launched and working, you have succeeded.

Now, instead of navigating hundreds of folders every single launch time, use the quick launch configurations in the top as shown in the picture above. Playing `RuneLite` will launch the client. Playing `install` will launch maven. Quick and easy. 

## Plugins:

If you're able to launch RuneLite successfully from Step 6 from above, plugin installation becomes really easy.

#### Installing Plugins: 

Remember the RuneLite class that you had to run in a previous step? In the same folder, there is a `plugins` folder. Navigate to `runelite > runelite-client > src > main > java > net > runelite > client` to find it.

![alt text](https://www.kthisiscvpv.com/qhEdn1555094916BYwZi.png "Plugins Folder")

When you want to install a plugin, drag your plugin inside the `plugins` folder.

![alt text](https://www.kthisiscvpv.com/sYryo1555095186LKRjq.png "Plugins Folder")

When prompted with a confirmation message, simply click `Okay`.

#### Uninstalling Plugins: 

Like above,navigate to `runelite > runelite-client > src > main > java > net > runelite > client`. 

However, this time, expand the `plugins` folder. You should see a bunch of plugins.

![alt text](https://www.kthisiscvpv.com/5hQIN1555095348xRGkD.png "Plugins Folder")

`Highlight` the plugin you wish to uninstall. Then press the `Delete` button your keyboard.

![alt text](https://www.kthisiscvpv.com/WfDNI1555095396EzX0w.png "Plugins Folder")

### Upgrading Plugins: 

Uninstall the plugin you wish to upgrade, then install the new patch. Simple.
