# General Mobile GM9PRO OOS (GSI)

*Uyarı*: *Bu rom **Generic System Image (GSI)** 'dır.*
*Tarafımca cihaza özgü özelleştirmeler ve hata düzeltmeleri yapılmıştır.*
* 01-08-2019 Güvenlik Yaması

## Çalışan Özellikler
-  Wi-Fi - Hotspot
-  Bluetooth
-  4G - LTE
-  Ses
-  Arama Servisleri
-  MTP - PTP - Tethering
-  Parmak İzi
-  Bildirim Işığı (LED)
-  Parlaklık Çubuğu
-  Sensörler
-  ADB Servisleri
-  Video Tuşu Medya Tuşu yapıldı.

## Bilinen Hatalar
-  VoLTE - VoWiFi 
-  FM Radio
## Rom Hakkında

- Android Sürümü : **9**
- C2API : **Açık**
- SELinux Durumu : **Permissive (Serbest)**
- Vendor : **9**
- Google Kamera : **Config ile Verimli Çalışıyor**
- Dolby : **Eklenmedi, Viper kullanabilirsiniz**
- PHH App : **Ekli**
- Source :  [OOS](https://sourceforge.net/projects/oemgsis/files/OxygenOS/OxygenOS-AB-9-20190930-ErfanGSI.img.7z/download)
- Kullanılan Fix Pack : [fixpack_gm9pro_sprout](https://github.com/zenlty/fixpack_gm9pro_sprout)

## Medya Tuşu Hakkında

Keycode cinsinden MEDIA_PLAY_PAUSE olan bu özelliğin işlevi şu şekildedir.

|Tek Basma| Çift Basma  | Basılı Tutma |
|--|--|--|
| Müziği Başlat - Durdur | Müziği Değiştir |Google Asistan


Bir nevi kulaklığın orta tuşunun gördüğü işlevi görür

## Otomatik Kurulum
Fastboot ile kurulum hazırladım.

Bunun için linkten romu indirip arşivi bir klasöre çıkartın. 

Windows kullanıcıları Driver kurulumunu yapmaları gerebilir.

Linux kullanıcılarının Driver kurulumu yapmasına gerek yok.

**Uyarı : Mümkünse USB 2.0 portunu kullanın, USB 2.0 portunuz yoksa USB çoğaltıcılar ile bağlantı kurun.**

**USB çoğaltıcılar genellikle 2.0 kullanırlar.**

- Cihazı kapatıp 5 - 6 saniye bekleyin.
- Ses kısma + Güç tuşuna basılı tutarak fastboot moduna geçin
-  **Dikkat Veri Kaybı olacaktır**
- `fastboot oem unlock-go` komutunu verin ve ardından telefondan ses tuşları ile "yes" seçeneğini güç tuşu ile seçin ardından ses kısma tuşuna basılı tutun
- Windows kullanıyorsanız install-windows.bat aracını çalıştırın ve kurulumun bitmesini bekleyin cihaz açılacaktır.
-  Linux kullanıyorsanız terminal ile bulunduğunuz dizine gelin
- `chmod a+x install_linux.sh`
- `.\install_linux.sh` çalıştırın ve kurulumun bitmesini bekleyin.
- 

## Manuel Kurulum

Windows kullanıcıları Driver kurulumunu yapmaları gerebilir.

Linux kullanıcılarının Driver kurulumu yapmasına gerek yok.

**Uyarı : Mümkünse USB 2.0 portunu kullanın, USB 2.0 portunuz yoksa USB çoğaltıcılar ile bağlantı kurun.**

**USB çoğaltıcılar genellikle 2.0 kullanırlar.**

- Cihazı kapatıp 5 - 6 saniye bekleyin.
- Ses kısma + Güç tuşuna basılı tutarak fastboot moduna geçin
-  **Dikkat Veri Kaybı olacaktır**
- `fastboot oem unlock-go` komutunu verin ve ardından telefondan ses tuşları ile "yes" seçeneğini güç tuşu ile seçin ardından ses kısma tuşuna basılı tutun
-  Windows kullanıyorsanız `start.bat` dosyasını çalıştırın.
- Linux kullanıyorsanız terminal ile bulunduğunuz dizine gelip libs klasörü içine girin.
- `fastboot flash system system.img`
- `fastboot flash vendor vendor.img`
- `fastboot flash boot boot.img`
- `fastboot erase userdata`
- `fastboot reboot`
