# rootsuzandroiduygulamasilme
Rootsuz Android Uygulama Silmek
https://www.youtube.com/watch?v=LQx9R3lIp74


İlk olarak adb.zip dosyasını indiriniz. 
( Ayrıca Link üzerinden https://developer.android.com/studio/releases/platform-tools sitesinde 'Download SDK Platform-Tools for Windows'  windows için indirebilirsiniz.)


![1](https://user-images.githubusercontent.com/62428397/183443335-1a6400e1-5ea8-4d5b-a8e5-b1f62ec121e5.png)

Resimde görüldüğü üzere dosyayı rardan çıkardıktan sonra içine girerek shift + mouse sağ click basınız.

Sonrasında PowerShell penceresini burada açına basınız.

Telefonu bağlamadan önce;

Ayarlar -> Telefon Hakkında Giriniz.


<img src="https://user-images.githubusercontent.com/62428397/183444645-c6a4931b-5448-4218-8102-99ad4edcb50a.jpg" width="200">

Yazılım Bilgileri Kısmına Basınız.

Yapım Numarası kısmına basarak geliştirici seçeneklerini açınız.

<img src="https://user-images.githubusercontent.com/62428397/183447429-16f217c1-d508-4c11-a5d3-e864feeb3937.png" width="200">

Sonrasında geliştiri seçeneklerini açınız.

<img src="https://user-images.githubusercontent.com/62428397/183445147-531055ba-4ab2-4ef6-bb83-cf13f2f51ea0.jpg" width="200">


Usb Hata Ayıklamasını resimde görüldüğü gibi etkinleştiriniz.

<img src="https://user-images.githubusercontent.com/62428397/183445516-6fa11295-d9c7-435f-a994-7f4a621c19d0.jpg" width="200">

Sonra telefonu bilgisayara bağlarken resimde görüldüğü üzere gelen izin isteğinde izin ver tuşuna basınız.

<img src="https://user-images.githubusercontent.com/62428397/183446081-817f6dd3-1725-4653-8d7d-eccc95155986.jpg" width="200">

Tekrardan bilgisayar ekranına döndükten sonra resimde de gördüğünüz gibi ./adb device yazdığımızda telefon bağlantısının kurulmuş olduğunu göreceksiniz.
![image](https://user-images.githubusercontent.com/62428397/183446486-4dd49803-120d-480d-9570-95d758611f03.png)

./adb shell komutunu yazarak, Android Debug Bridge terminalini başlatınız.

![image](https://user-images.githubusercontent.com/62428397/183449346-593014c8-ad5c-41ca-90d6-9a582412f1de.png)


terminal başladıktan sonra ' pm list packages ' komutunu yazarak telefonunuzda yüklü tüm uygulamaları görebilirsiniz.
( Örnek: Sadece google uygulamalarını görmek için " pm list package | grep 'google' " yazınız. )

![image](https://user-images.githubusercontent.com/62428397/183449607-aa209121-8592-42ef-acee-3289ba8a90e6.png)


Bir uygulamayı silmek için aşağıdaki örnekteki kodu yazabilirsiniz.

pm uninstall -k --user 0 com.google.android.youtube

Yukarıdaki örnekte com.google.android.youtube yazarak youtube uygulamasını silmiş oluyoruz.
Başka uygulama silmek için pm uninstall -k --user 0 yazısından sonra ' pm list packages ' komutuyla getirmiş olduğumuz uygulama bilgilerinden uygulama silebilirsiniz.




