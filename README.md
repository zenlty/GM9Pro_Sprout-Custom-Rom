# General Mobile GM9PRO Pixel (GSI)

*Uyarı*: *Bu rom **Generic System Image (GSI)** 'dır.*
*Tarafımca cihaza özgü özelleştirmeler ve hata düzeltmeleri yapılmıştır.*

## Çalışan Özellikler
-  Wi-Fi - Hotspot
-  Bluetooth
-  4G - LTE
-  Always on Display (AOD)
-  Ses
-  Arama Servisleri
-  MTP - PTP - Tethering
-  Parmak İzi
-  Bildirim Işığı (LED)
-  Parlaklık Çubuğu
-  Sensörler
-  ADB Servisleri

## Bilinen Hatalar
-  VoLTE - VoWiFi 
-  FM Radio
-  Otomatik Parlaklık + C2API [PATCH](https://github.com/zenlty/GM9Pro_Sprout-Custom-Rom/releases/download/10-2019-10-06/Pixel_Ekim_Patch.zip) ile düzeliyor
## Rom Hakkında

- Android Sürümü : **10**
- C2API : **Açık**
- Vendor : **9 + AOD Destekli**
- Root : **Magisk**
- Google Kamera : **Config ile Verimli Çalışıyor**
- Dolby : **Eklenmedi, Viper kullanabilirsiniz**
- PHH App : **Ekli**
- Source :  [Pixel](https://mirrors.lolinet.com/firmware/gsi/Pixel/Pixel-AB-10-20191008-ErfanGSI.img.7z)
- Kullanılan Fix Pack : [fixpack_gm9pro_sprout](https://github.com/zenlty/fixpack_gm9pro_sprout)


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
