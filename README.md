# Raspberry-pi-VR
This project allows anyone with a raspberry pi and $300 to create their own lighthouse track vr headset using several software and steamvr dependencies as I just said you will need a pc capable of running vr for me a gtx 1060 6gb and a ryzen 3 4100 is enough for the project I will give you the instructions to follow below
1. Things you'll need:
You'll need a 3D printer (you can find one on eBay for $100), a PC capable of running VR and time.
2. buy the different parts:
a raspberry pi 4 at least 2gb of ram here is a link to get it https://www.kubii.com/en/nano-computers/2771-raspberry-pi-4-model-b-2gb-5056561800332.html?gad_source=1&gad_campaignid=22521945089&gbraid=0AAAAApc7Y9mLVbye3ZxcucaYQkDJoqCpY&gclid=Cj0KCQjw9O_BBhCUARIsAHQMjS4RG0_S2pPgrAOO9RTvORaFUgDZneCOPqlCCog575-CZGT-LK1Lwa8aAoLSEALw_wcB, an sd card of at least 32gb a link to get it https://www.amazon.com/SanDisk-MicroSDHC-Memory-Adapter-Approved/dp/B08GY9NYRM/ref=sr_1_6_mod_primary_new?adgrpid=55600119749&dib=eyJ2IjoiMSJ9.vRRteS1syrRQ4bNYx6_9cd59D1VFxzZxv85RwTUOQkHgHV2qXg, a 3.5 inch screen, here is the screen that I personally used https://www.amazon.com/gp/product/B0DRF9Q566/ref=ox_sc_act_title_1?smid=A31ODO8OD3XQQH&psc=1, a vr headset like this one (we will just take the lenses) https://www.amazon.com/NK-Lunettes-pour-smartphone-intelligentes/dp/B09GFLD2VG/ref=sr_1_6?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1JBG82G1TXAC3&dib=eyJ2IjoiMSJ9.7fCg9ZLkOPGPbEYJhPC8ginptCEIWO3cSo0ykJPzo3HMQsBoj_-mu8v62v0r_PLvA1UyAwdtnOFsErj5gycgfavoV7J-ULuGBmnmWyT97UyYbRXbyeaV6W2ECRliJhk8_D7ankIrfeWmza0EQbAhXjn3sfjVcOa-nNOy9DH41wOks-p4lcXxhUTMvKqzFtV6RMedLnP7Op7pOhA1ZIAa1hnjW3Dj1FjZenk9COx3M_4_8T5YfN9PjuIFB7rAR77xt4vVyNrdfWdj0lvsTDSw_lRMU6t-QFxATZGBXuBdImI.uAFkEPDQtxL4eNFjCvTm13L0lZn2YNSdnYX3F-U8Loo&dib_tag=se&keywords=casque%2Bvr%2Bpour%2Btelephone&qid=1748795709&sprefix=casque%2Bvr%2Bpour%2Btelephone%2Caps%2C327&sr=8-6&th=1,for the most expensive parts you will need a base station and a tracker of vive, you can use 1.0 base station

   ![image](https://github.com/user-attachments/assets/ed941fc7-b665-4c6b-868d-bcd0350caccf)

   or 2.0 base station

   ![image](https://github.com/user-attachments/assets/4f288e35-41b8-47d8-8b62-5beb0887c92a)

but you can't use 2.0 tracker, you have to use 3.0 (I want to say that is not necessary to have them but that recomended if you want to have a 6dof tracking if your budget is tight you can use 3dof tracker like for example a slimevr tracker or a joycon: to connect a joycon to slimevr https://www.youtube.com/watch?v=E-BFpbL1ae8&t=437s
3. 3D printing:
(the 3d files are based on the free 3d files from bigscreen beyond) for the 3d printing I will give you the stl and cad files in the release part I use 1. 2. 3D disigne for the cad files I am sorry but the cad files can only be opened by 1. 2. 3d disigne from what I know. the 3d files should look like this

![Capture d'écran 2025-06-01 200848](https://github.com/user-attachments/assets/fae83927-09b9-4878-ac52-f37666f57f95) ![image](https://github.com/user-attachments/assets/9e0ec8cb-c227-4068-9a05-255380534478) ![image](https://github.com/user-attachments/assets/b495b8b9-e4c1-4fee-8134-73a92854d6ba) ![image](https://github.com/user-attachments/assets/d3225eb8-ce1b-4c6d-a1e8-45d74be83a65) ![image](https://github.com/user-attachments/assets/aed0ddeb-2f41-418d-afea-c27d9eda48f8)

5. software:
For the PC software you will use vridge (https://riftcat.com/) it is available on steam you will also have to install steamvr and apply the changes to the steamvr configuration as I will show you in the next part, for the raspberry side you will install android and two apk I will put them in the release section

6. tracking overrides:
To make SteamVR believe that your tracker is your VR headset, you will have to change some setting in the SteamVR configuration. First, you will have to change the following configuration to make steamvr believe that your tracker is your vr headset you will have to change some setting in the steamvr config, first you will have to change the following config, go to C:\Program Files (x86)\Steam\steamapps\common\SteamVR\resources\settings and open default.vrsettings with notepad and change the line "requireHmd": true, to "requireHmd": false, and change the line "activateMultipleDrivers": false, to "activateMultipleDrivers": true, save and close the file it should look like this

![image](https://github.com/user-attachments/assets/578e7d87-477b-4d04-a8b3-08a0d5b0c354) ![image](https://github.com/user-attachments/assets/dd414f9a-1128-46f3-96f2-ba2dfbc62823)

Once that's done, go to C:\Program Files (x86)\Steam\config and open the steamvr.vrsettings file and add this line 
},
"TrackingOverrides": {
"/devices/..../....": "/user/head"
It should look like this 

![image](https://github.com/user-attachments/assets/34ea4d28-9e12-4d8c-bc33-db7e45b3d75f)

To run it, you'll need to know your tracker's ID. To do this, start SteamVR and click on the SteamVR version number. Go to Devices and Manage Trackers. Find your tracker's ID, for example, this one ![image](https://github.com/user-attachments/assets/dbeca51b-ac1d-4712-8ae1-ffa1870b37dc) when you have found the ID of your tracker, like in the image you will add /devices/lighthouse/....... to tracking overrides like this

![image](https://github.com/user-attachments/assets/00ef5c4a-a1df-4ea9-9618-499b6fdb960b)

save and close the file and that's it (If you use slimevr trackers, it's the same thing, but you replace /devices/lighthouse/....... with /devices/slimevr/human://....)

face tracking:
If you want face tracking you will need to install VRCFT (obtainable on steam) and the Babble add-on ![image](https://github.com/user-attachments/assets/36fc8ca7-bef0-4607-8d99-eadeafe9a6bb)
and Project Babble (I will put them in release) You will also need a camera or a phone, to mount the camera on the VR headset You will need to make sure it has a good viewing angle on your mouth and glue it whit hot glue

final result:
If you did everything right it should look like this [insert image here]

tutorial:
just follow the instructions I said before and glue the 3d parts together with a glue gun
