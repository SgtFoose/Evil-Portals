## Evil Portals

[Evil Portals](https://github.com/SgtFoose/Evil-Portals) is a collection of portals that can be loaded into the Evil Portal module and can be used for phishing attacks against WiFi clients in order to obtain credentials or infect the victims with malware using the [Hak5](https://hak5.org/) [WiFi Pineapple](https://wifipineapple.com/) [Tetra](http://hakshop.myshopify.com/products/wifi-pineapple?variant=11303845317) and [Nano](http://hakshop.myshopify.com/products/wifi-pineapple?variant=81044992).

This project has been tested on the Pineapple MK7 with firmware 1.0.2 stable only!! 


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
Evil Portals is distributed under the GNU GENERAL PUBLIC LICENSE v3. See [LICENSE](hhttps://github.com/SgtFoose/Evil-Portals/LICENSE) for more information.

#### Disclaimer
* Usage of Evil Portals for attacking infrastructures without prior mutual consistency can be considered as an illegal activity. It is the final user's responsibility to obey all applicable local, state and federal laws. Authors assume no liability and are not responsible for any misuse or damage caused by this program.

---

Discussion thread - [Hak5 Forums](https://forums.hak5.org/index.php?/topic/39856-evil-portals/)

### Videos
https://www.youtube.com/watch?v=XyWYiM48F_E&ab_channel=SgtFoose
