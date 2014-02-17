Android Camera Util
===================

It seems to be the simplest thing in the world: taking a picture within your Android app using the default camera activity. However, there are many pitfalls which are covered in several posts across the web as, for instance, null intents being passed back, the orientation of the picture not being correct or OutOfMemoryErrors. Finally, I managed to get it working on a wide variety of devices (see list below) and I wanted to share my solution with you. The code is partially based on the following posts:

* [Camera Force Closing issue in Samsung Galaxy S3 version 4.1.1](http://stackoverflow.com/questions/14495304/camera-force-closing-issue-in-samsung-galaxy-s3-version-4-1-1)
* [Null Intent passed back On Samsung Galaxy Tab](http://kevinpotgieter.wordpress.com/2011/03/30/null-intent-passed-back-on-samsung-galaxy-tab/)

I tried hard to avoid implementing different strategies based on the device configuration (e.g. manufacturer, model, ...). Unfortunately, I did not get around it. Going through hundreds of posts and talking to several developers, nobody found a solution that works on all devices without implementing device configuration specific code.


The code was _successfully_ tested on the following devices with Android API-Level >= 8 and stock Android.

* HTC Desire S
* HTC Desire X
* HTC Sensation
* HTC One
* HTC One Mini
* HTC One S
* HTC One SV
* HTC One X
* HTC One X+
* HTC One V
* Huawei y300-0100
* Huawei p6-u06
* Huawei u8510
* Huawei u9200
* LGE Nexus 4
* LGE Nexus 5
* LGE Optimus L3 (lg-e400)
* LGE Optimus L7 (lg-p700)
* LGE Optimus L7 II (lg-p710)
* LGE Optimus 4X (lg-p880)
* LGE Optimus Black (lg-p970)
* LGE Prada (lg-p940)
* LGE G2 (lg-d802)
* Medion p4013
* Motorola Defy (mb525)
* Samsung Galaxy W (gt-i8150)
* Samsung Galaxy Ace 2 (gt-i8160)
* Samsung Galaxy S3 mini (gt-i8190)
* Samsung Galaxy S (gt-i9000)
* Samsung Galaxy S Plus (gt-i9001)
* Samsung Galaxy SL (gt-i9003)
* Samsung Galaxy S2 (gt-i9100)
* Samsung Galaxy S2 Plus (gt-i9105p)
* Samsung Galaxy S3 (gt-i9300)
* Samsung Galaxy S3 mini (gt-i8190n)
* Samsung Galaxy S4 (gt-i9505)
* Samsung Galaxy S4 Active (gt-i9295)
* Samsung Galaxy Note (gt-n7000)
* Samsung Galaxy Note 2 (gt-n7100 and gt-n7105)
* Samsung Galaxy Note 10.1 (gt-n8000)
* Samsung Galaxy Tab (gt-p1000)
* Samsung Galaxy Tab 2 (gt-p3110)
* Samsung Galaxy Tab 3 (sm-t315)
* Samsung Galaxy Fit (gt-s5670)
* Samsung Galaxy Ace (gt-s5830)
* Samsung Galaxy Ace (gt-s5830i)
* Samsung Galaxy Young Duos (gt-s6312)
* Samsung Galaxy Mini (gt-s6500)
* Samsung Galaxy Note 3 (sm-n9005)
* Samsung Galaxy Nexus
* Sony Xperia Z (c6603)
* Sony Xperia Z1 (c6903)
* Sony Xperia Ray (st18i)
* Sony Xperia U (st25i)
* Sony Xperia Go (st27i)
* Sony Xperia Tipo (st21i)
* Sony Ericsson Xperia S (lt26i)
* Sony Ericsson Xperia Arc S (st18i)


With regards to custom Roms, the code  was _successfully_ tested on the following devices with Android API-Level >= 8 and the CyanogenMod.

* Samsung Galaxy S Plus (gt-i9001)



Please feel free to check out the code. [CameraIntentHelperActivity](https://github.com/ralfgehrer/AndroidCameraUtil/blob/master/src/de/ecotastic/android/camerautil/lib/CameraIntentHelperActivity.java) provides the main functionality.

[TakePhotoActivity](https://github.com/ralfgehrer/AndroidCameraUtil/blob/master/src/de/ecotastic/android/camerautil/example/TakePhotoActivity.java) is an example Activitiy on how to use the CameraIntentHelperActivity.
