# Forked from 

https://github.com/liuyufei/SSLKiller

nothing changed only added a compiled version of apk.

compiled with :

- Android Studio 3.0.1
- Android SDK 5.1(Lollipop)
- Gradle 3.0.1

tested on Android 5.1.1(MIUI 7 8.8.8)with Xposed 3.0 alpha4,should also works on other similar device.

**You can download apk from:**

**[Here](https://github.com/Arryboom/SSLKiller/raw/master/releaseAPK/SSLKILLER.apk)**

- File: SSLKILLER.apk
- Size: 1055547 bytes
- Modified: 24-02-2018, 11:02:55
- MD5: 95EC8BBCAA88BD2E006A57B5E6B04892
- SHA1: 40DE390F07085F56273D4935953E9661BC7A5B1C
- CRC32: F7C8E05E

# SSLKiller

SSLKiller is used for killing SSL verification functions on **Android** client side. With SSLKiller, You can intercept app's **HTTPS** communication packages between the client and server. This project is very helpful for those who wants to analysis the network communications in android apps but with HTTPS deployment.

This project is build as a Xposed module. Before using it, you have to install **[Xposed](http://repo.xposed.info/module/de.robv.android.xposed.installer)** on your Android device first!

Burp Suite can help us to deploy a MITM and intercept transparent http packages. When meets https transaction, burp uses a fake server cert to communicate with the client. If app has a uncorrect cert verification process (e.g. an empty TrustManager implementation) the https packages can be intercepted by burp but if app do the right verification, burp will alert connection failed error. SSLKiller can fix this problem and let all https transaction of the app displayed in burp.

![preview](imgs/preview.jpeg)




