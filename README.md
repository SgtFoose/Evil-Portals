## Foose Evil Portals

[Foose Evil Portals](https://github.com/SgtFoose/Evil-Portals) is my collection of portals that can be loaded into the Evil Portal module and can be used for phishing attacks against WiFi clients in order to obtain credentials or infect the victims with malware using the [Hak5](https://hak5.org/) [WiFi Pineapple Mark VII](https://wifipineapple.com/) 

These projects have been tested on the Pineapple MK7 with the following firmwares:

1.0.0 not tested

1.0.1 not tested

**1.0.2 Works!** [Link](https://downloads.hak5.org/api/devices/wifipineapplemk7/firmwares/1.0.2-stable)

**1.1.1 Works!** [Link](https://downloads.hak5.org/api/devices/wifipineapplemk7/firmwares/1.1.1-stable)

2.0.0 Works but requeire special settings, recommended to wait till stable release.

2.1.3 Stable 11/03/2025 Found some issues running the portals. Investigating right now.
When adding the portal to the MK7, it does work and run but it appears as Portal Type BASIC so you cant hit the Preview and View Log buttons anymore.

Kleo / Hak5 seems to have chagend the layout of the .ep file. I have tried to Add a new portal from the tool itself to be able to update my portals .ep files, but his seems not to have the expected result and the Module would still show my portals as type BASIC.

To be continued!!


---

#### Installation of the Portals
Installation can be done in atleast two ways:

<br />

**Option 1: From your PC/Desktop:**

Download the repository form [Github](https://github.com/SgtFoose/Evil-Portals) (green code button top right / download ZIP)

Extract the files on your computer (e.g. \Downloads\Evil-Portals-main\Evil-Portals-main\Portals).

You can use [Filezilla](https://filezilla-project.org/) to copy the portals on the Pineapple MK7 in folder /root/portals/.
Make sure to only copy the Portals, not the entire folder! On the MK7 it should look like this example: /root/portals/ziggo-login/ (not /root/portals/Evil-Portals-main\Evil-Portals-main\Portals\ziggo-login).

Host: sftp://172.16.42.1 Username: root Password: yourpassword Port: 22

<br />

![image](https://github.com/SgtFoose/Evil-Portals/assets/17387175/dae3217b-9399-454a-96f6-376ce52966f9)


**Option 2: From your Pineapple Console:**

You need a program to unzip the portals. I used InfoZIP's (search for "unzip"), which can be found in your Packages page of the Pineapple. Make sure this is installed before you continue!

Next, jump in the Pineapple Console and download the portals from my Github using the following command:

wget https://github.com/SgtFoose/Evil-Portals/archive/refs/heads/main.zip -O /root/portals/portals.zip

---

Next, we need to verify if downloading suceeded. 

Type these console commands:

**cd ..**

**cd root** (it looks like nothing happens with this step, please continue)

**cd portals**

**ls** (to verify if portals.zip is in your folder, if succeeded, proceed to the next steps)

You should see this:

**root@mk7:~/portals# ls**

**portals.zip**

**root@mk7:~/portals#**

---

**Alternative way of verifying:**

With the Module "Cabinet" from the Download Modules page, you can browse / verify the content in this folder:

**/root/portals**

In here, you will find a new file called "Portals.zip". If success, jump back in the Pineapple console and cd back into this "/root/portals" folder.

---

Next, we need to unzip the portals with the following console command:

**unzip portals.zip** (this will start extracting the portals into a folder named "Evil-Portals-main")

---

Next, we need to move the downloaded portals into the correct folder. 
Again we have alteast two options:

**Option 1:** 

Use your Pineapple's browser called "Cabinet" to move the desired Portals from this folder "/root/portals/Evil-Portals-main/Portals/mcdonalds-login" (e.g. mcdonalds-login) to folder "/root/portals/".

<br />

**Option 2:**

If you want to copy all availlible portals, use this command in the Pineapple console:

**mv -v -i /root/portals/Evil-Portals-main/Portals/* /root/portals/**

If you just want one of the portals, simply replace the "*" with the name of the desired Portal:

**mv -v -i /root/portals/Evil-Portals-main/Portals/mcdonalds-login /root/portals/**

---

Next, we need to verify the content of the Portals folder with command:

**ls**

You should see something like this:

**root@mk7:~/portals# ls**

**Evil-Portals-main  mcdonalds-login    portals.zip        ziggo-login**

**root@mk7:~/portals#**

If everything worked out well, please continue!

Optional and recommend is to remove the Evil-Portals-main folder which is no longer needed with command:

**rm -r Evil-Portals-main**

---

#### Usage

Ok, downloading and installing is now complete!

Next, close the console and open your Evil Portal and they should now appear. If not, jump out of the Portal Page and come back which will refresh the portal list.

If the new portal does not appear, just add a BASIC portal from the portals menu options. I found out this way of dealing with it was required on Firmware 2.1.3 stable. Refresh the page and both your new Portal and te BASIC portal should show.

![image](https://github.com/SgtFoose/Evil-Portals/assets/17387175/53c3f69f-27bf-4769-8246-cb88f8956963)


Make sure both the Evil Portals Web Server and Module have started and make sure your portal is "**Activated**" which can be verified using the "Preview" button.

Finally after gathering credentials, captured data will be shown as a notification on the WiFi Pineapple web interface. 

Logs are found at Modules > Evil Portal > Logs > View.

---

#### Firmware

If you like to up or downgrade your Mark VII, I strongly recoomend to use [these](https://docs.hak5.org/wifi-pineapple/faq/factory-reset-and-recovery) steps first.

Then, use one of the [.bin](https://downloads.hak5.org/api/devices/wifipineapplemk7/firmwares) files to upgrade. 

---

#### License

Evil Portals is distributed under the GNU GENERAL PUBLIC LICENSE v3. See [LICENSE](https://github.com/SgtFoose/Evil-Portals/blob/main/LICENSE) for more information.

---

#### Disclaimer

Usage of Evil Portals for attacking infrastructures without prior mutual consistency can be considered as an illegal activity. 
It is the final user's responsibility to obey all applicable local, state and federal laws. 
Authors assume no liability and are not responsible for any misuse or damage caused by this program.

---

#### Discussion thread

[Hak5 Forums](https://forums.hak5.org/index.php?/topic/39856-evil-portals/)

---

#### Videos

* [Ziggo Evil Portal](https://youtu.be/knW2t2AYfGk)
* [How to build your own Evil Portal](https://youtu.be/r6YXPGYmK0w)
* [Hotel Evil Portal](https://www.youtube.com/watch?v=XyWYiM48F_E&ab_channel=SgtFoose)

---

#### Screenshots

![alt text](https://user-images.githubusercontent.com/17387175/160284637-2b6bd6c3-d85c-40f2-b6f5-ee8d291dd87b.png?raw=true)
![alt text](https://user-images.githubusercontent.com/17387175/158378292-32af4781-31b7-4ce8-aae0-f09285bc9262.png?raw=true)

---

#### Credits

[Kleo Bercero](https://github.com/kleo/evilportals)

---

[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=SgtFoose)](https://github.com/anuraghazra/github-readme-stats)

<br />

#### 📺 Latest YouTube Videos

<!-- YOUTUBE:START -->
- [Hak5 Wifi Pineapple MKVII Tutorials](https://youtube.com/playlist?list=PL-Yn2GfVAO9hhArZujZQ7RgEgbLDldM7_)
<!-- YOUTUBE:END -->

➡️ [more videos...](https://youtube.com/SgtFoose)

---

### Youtube:

[![YouTube Channel Subscribers](https://img.shields.io/youtube/channel/subscribers/UCDCHcqyeQgJ-jVSd6VJkbCw?logo=youtube&logoColor=red&style=for-the-badge)][youtube]

[youtube]: https://youtube.com/SgtFoose
