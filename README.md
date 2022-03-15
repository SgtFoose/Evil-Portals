## Evil Portals

[Foose Evil Portals](https://github.com/SgtFoose/Evil-Portals) is my collection of portals that can be loaded into the Evil Portal module and can be used for phishing attacks against WiFi clients in order to obtain credentials or infect the victims with malware using the [Hak5](https://hak5.org/) [WiFi Pineapple Mark VII](https://wifipineapple.com/) 

This project has been tested on the Pineapple MK7 with these firmwares:

1.0.0 not tested

1.0.1 not tested

1.0.2 Wokrs! (15-03-2022)

1.1.1 not working (10-03-2022)

2.0.0 not working (14-03-2022)


---

#### Usage

Download the repository form https://github.com/SgtFoose/Evil-Portals (green code button top right / download ZIP)

Extract the files on your computer (e.g. \Downloads\Evil-Portals-main\Evil-Portals-main\Portals).

You can use [Filezilla](https://filezilla-project.org/) to copy the portals on the Pineapple MK7 in folder /root/portals/.
Make sure to only copy the Portals, not the entire folder! On the MK7 it should look like this example: /root/portals/ziggo-login/ (not /root/portals/Evil-Portals-main\Evil-Portals-main\Portals\ziggo-login).

Host: sftp://172.16.42.1 Username: root Password: yourpassword Port: 22

Finally on the WiFi Pineapple web interface, start the Evil Portal module and then activate the portal you wish to use.

After gathering credentials, captured data will be shown as a notification on the WiFi Pineapple web interface. Logs are found at Modules > Evil Portal > Logs > View.

---
#### License
Evil Portals is distributed under the GNU GENERAL PUBLIC LICENSE v3. See [LICENSE](https://github.com/SgtFoose/Evil-Portals/blob/main/LICENSE) for more information.

#### Disclaimer
* Usage of Evil Portals for attacking infrastructures without prior mutual consistency can be considered as an illegal activity. It is the final user's responsibility to obey all applicable local, state and federal laws. Authors assume no liability and are not responsible for any misuse or damage caused by this program.

---

Discussion thread - [Hak5 Forums](https://forums.hak5.org/index.php?/topic/39856-evil-portals/)

### Videos
https://www.youtube.com/watch?v=XyWYiM48F_E&ab_channel=SgtFoose

### Credits
https://github.com/kleo/evilportals

### Screenshots
![alt text](https://user-images.githubusercontent.com/17387175/158378292-32af4781-31b7-4ce8-aae0-f09285bc9262.png?raw=true)
