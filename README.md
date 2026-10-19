# Qufu Codex Dashboard

A compact desktop companion for tracking Codex sessions, token usage and account limits.

**Version 1.0 Â· Windows & Linux Â· Author: [alper@qufu.io](mailto:alper@qufu.io)**

[Downloads / Ä°ndir](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases) Â· [TÃ¼rkÃ§e](#tÃ¼rkÃ§e) Â· [English](#english) Â· [qufu.io](https://qufu.io)

<p align="center">
  <img src="docs/images/dashboard-1.0.png" width="300" alt="Qufu Codex Dashboard 1.0 showing session tokens, last request cost, context usage and account limits">
</p>

> **1.0 gÃ¼ncelleme sÃ¼rÃ¼mÃ¼ son test aÅŸamasÄ±nda. Kurulum paketleri test onayÄ±ndan sonra Releases bÃ¶lÃ¼mÃ¼ne eklenecek.**
> **The updated 1.0 build is undergoing final testing. Installers will appear in Releases after acceptance.**

## TÃ¼rkÃ§e

Qufu Codex Dashboard, Codex kullanÄ±mÄ±nÄ± kÃ¼Ã§Ã¼k bir masaÃ¼stÃ¼ penceresinden takip etmeni saÄŸlar. Tauri 2 ile geliÅŸtirilmiÅŸtir; Windows ve Linux Ã¼zerinde Ã§alÄ±ÅŸÄ±r.

### Ã–zellikler

- Workspace ve session seÃ§imi; arÅŸivlenmiÅŸ, internal ve subagent kayÄ±tlarÄ±nÄ± ana listeden ayÄ±ran otomatik filtreleme.
- Toplam ve son tamamlanan model yanÄ±tÄ± iÃ§in Input, Output, Cache tokenlarÄ± ve tahmini USD maliyeti.
- Son 60 saniyeden hesaplanan canlÄ± token/saniye deÄŸeri.
- Ã–lÃ§Ã¼lmÃ¼ÅŸ context kullanÄ±mÄ± ve session tarafÄ±ndan bildirilen context kapasitesi.
- 5 saatlik ve haftalÄ±k hesap limitleri, reset sayaÃ§larÄ± ve veri yeterliyse aÃ§Ä±kÃ§a iÅŸaretlenmiÅŸ tahmini token eÅŸdeÄŸerleri.
- Detaylar panelinde subagent tÃ¼ketimi, model dÃ¶kÃ¼mÃ¼ ve hesap abonelik tÃ¼rÃ¼.
- Her zaman Ã¼stte, sistem tepsisi, hatÄ±rlanan pencere ayarlarÄ±, ÅŸeffaflÄ±k, koyu/aÃ§Ä±k tema ve TÃ¼rkÃ§e/Ä°ngilizce dil seÃ§imi.
- VarsayÄ±lan kapalÄ± Auto Follow Beta; seÃ§ili Desktop session doÄŸrulanamÄ±yorsa manuel seÃ§imi korur.

### Ä°ndirme ve kurulum

Uygulama **Ã¼cretsizdir ve kapalÄ± kaynaklÄ±dÄ±r**. Public daÄŸÄ±tÄ±m deposundan GitHub hesabÄ± veya davet gerektirmeden indirebilirsin. Kaynak kodu bu depoda paylaÅŸÄ±lmaz.

1. [1.0 sÃ¼rÃ¼mÃ¼nÃ¼ aÃ§](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases).
2. **Assets** bÃ¶lÃ¼mÃ¼nÃ¼ geniÅŸlet.
3. Ä°ÅŸletim sistemine uygun paketi indir:

| Platform | Paket | Kurulum |
| --- | --- | --- |
| Windows x64 | `*_x64-setup.exe` | DosyayÄ± Ã§alÄ±ÅŸtÄ±r; kurulumdan sonra BaÅŸlat menÃ¼sÃ¼nden aÃ§. |
| Ubuntu / Debian amd64 | `*_amd64.deb` | `sudo apt install ./indirilen-dosya.deb` |
| Linux x64 | `*_amd64.AppImage` | `chmod +x indirilen-dosya.AppImage` ardÄ±ndan dosyayÄ± Ã§alÄ±ÅŸtÄ±r. |

**Gereksinimler:** Yerel session verisi oluÅŸturan Codex kurulumu. CanlÄ± hesap limitleri iÃ§in oturum aÃ§Ä±lmÄ±ÅŸ Codex CLI (`codex` komutu PATH Ã¼zerinde) gerekir. Windows kurucusu WebView2'yi kontrol eder; eksikse internetten indirip otomatik kurar. WebView2 kurulumu baÅŸarÄ±sÄ±z olursa uygulama kurulumu durur. Linux'ta WebKitGTK 4.1 ve Ã§alÄ±ÅŸan bir masaÃ¼stÃ¼ oturumu gerekir; GNOME'da tray iÃ§in AppIndicator eklentisi gerekebilir. Wayland, pencere konumunu ve her zaman Ã¼stte davranÄ±ÅŸÄ±nÄ± sÄ±nÄ±rlandÄ±rabilir.

**GÃ¼ncelleme:** Eski uygulamayÄ± tray menÃ¼sÃ¼ndeki **Quit / Ã‡Ä±kÄ±ÅŸ** ile kapat, ardÄ±ndan yeni kurulumu Ã§alÄ±ÅŸtÄ±r. Pencerenin X dÃ¼ÄŸmesi uygulamayÄ± tray'e gizler.

### KullanÄ±m

Ãœstteki workspace/session adÄ±na tÄ±klayÄ±p takip edeceÄŸin session'Ä± seÃ§. Detaylar paneli model ve subagent dÃ¶kÃ¼mÃ¼nÃ¼ gÃ¶sterir. Ayarlardan dil, tema, ÅŸeffaflÄ±k ve her zaman Ã¼stte seÃ§eneklerini deÄŸiÅŸtirebilirsin.

Alt satÄ±r son limit gÃ¼ncelleme saatini gÃ¶sterir; eski veride ne kadar sÃ¼re geÃ§tiÄŸi belirtilir.

VarsayÄ±lanlar: Ä°ngilizce, %33 ÅŸeffaflÄ±k, 300 piksel geniÅŸliÄŸinde kompakt gÃ¶rÃ¼nÃ¼m. YÃ¼kseklik iÃ§eriÄŸe uyar; pencere ve sonraki tercihler hatÄ±rlanÄ±r. Context %80'i, hesap limitleri %90'Ä± aÅŸÄ±nca ilgili bar ve yÃ¼zde uyarÄ± rengine dÃ¶ner.

### Veriler ve hesaplama

- Yerel Codex metadata ve session kayÄ±tlarÄ± salt okunur kullanÄ±lÄ±r. `CODEX_HOME` ayarlÄ±ysa bu klasÃ¶r, yoksa `~/.codex` okunur. Liste keÅŸfinde tarih sÄ±nÄ±rÄ± veya elle yazÄ±lmÄ±ÅŸ session adlarÄ± yoktur.
- Cache, Input'un; reasoning, Output'un alt kÃ¼mesidir. Toplamda tekrar eklenmez. Ana session ve subagent tÃ¼ketimleri ayrÄ± sunulur.
- Bilinmeyen kullanÄ±m veya fiyat sÄ±fÄ±r gÃ¶sterilmez. Son istek, son tamamlanan **model yanÄ±tÄ±dÄ±r**; bir kullanÄ±cÄ± mesajÄ± birden fazla model yanÄ±tÄ± iÃ§erebilir.
- USD tutarlarÄ± API eÅŸdeÄŸeri tahmindir; abonelik faturasÄ± deÄŸildir. Resmi [OpenAI fiyatlarÄ±](https://developers.openai.com/api/docs/pricing) her aÃ§Ä±lÄ±ÅŸta kontrol edilir; eriÅŸilemezse son geÃ§erli fiyat, ilk aÃ§Ä±lÄ±ÅŸta ise dahil edilen fiyat tablosu kullanÄ±lÄ±r.
- Context miktarÄ± Ã¶lÃ§Ã¼lmÃ¼ÅŸ deÄŸerdir. Kapasite abonelikten tahmin edilmez.
- Hesap limitleri `account/rateLimits/read` Ã¼zerinden alÄ±nÄ±r. OpenAI sabit token kotasÄ± bildirmez. `â‰ˆ` iÅŸaretli miktarlar, yerel fiyat aÄŸÄ±rlÄ±klÄ± kalibrasyondan tahmini token eÅŸdeÄŸeridir; resmi kota veya hesap genelinde Ã¶lÃ§Ã¼lmÃ¼ÅŸ harcama deÄŸildir. Yeterli/gÃ¼venilir veri yoksa miktarlar bilinmiyor gÃ¶sterilir. BaÅŸka cihaz ve bulut kullanÄ±mÄ± tahminlerin doÄŸruluÄŸunu etkileyebilir.
- Yerel kullanÄ±m kaydÄ± bulunmayan bulut/ChatGPT sohbetleri listelenmez. Auto Follow doÄŸrulanmÄ±ÅŸ Desktop seÃ§imi bulunamazsa manuel kalÄ±r.

### Gizlilik ve paylaÅŸÄ±m

Uygulama konuÅŸmalarÄ± ve kullanÄ±m kayÄ±tlarÄ±nÄ± bir dashboard sunucusuna yÃ¼klemez; kimlik doÄŸrulama token dosyalarÄ±nÄ± okumaz. AÄŸ eriÅŸimi resmi fiyat kontrolÃ¼, kurulu Codex'in hesap limit okuyucusu ve GitHub gÃ¼ncelleme kontrolÃ¼/indirmesi iÃ§indir.

Ayarlar â†’ **GÃ¼ncellemeleri kontrol et** ile yeni sÃ¼rÃ¼mÃ¼ sorgulayabilirsin. Yeni sÃ¼rÃ¼m bulunduÄŸunda **Ä°ndir ve kur** dÃ¼ÄŸmesine tÄ±klaman gerekir; kurulum kendiliÄŸinden baÅŸlamaz. Paket imzasÄ± ve imzalanmÄ±ÅŸ sÃ¼rÃ¼m numarasÄ± doÄŸrulanÄ±r. Windows kurulum sÄ±rasÄ±nda kapanabilir; Linux'ta uygulama yeniden baÅŸlatÄ±lÄ±r. GitHub dÃ¼ÄŸmesiyle tÃ¼m sÃ¼rÃ¼mleri tarayÄ±cÄ±da aÃ§abilirsin. Ä°nternet veya yayÄ±n manifesti eriÅŸilemezse kontrol baÅŸarÄ±sÄ±z olarak gÃ¶sterilir; uygulama gÃ¼ncelmiÅŸ gibi davranmaz.

Uygulama Ã¼cretsiz kullanÄ±labilir; kaynak kodu, deÄŸiÅŸtirme, yeniden daÄŸÄ±tma veya satÄ±ÅŸ hakkÄ± verilmez. AyrÄ±ntÄ±lar iÃ§in [kullanÄ±m lisansÄ±nÄ±](LICENSE) incele.

## English

Qufu Codex Dashboard is a compact Tauri 2 desktop monitor for local Codex usage on Windows and Linux.

### Features

- Workspace/session picker with automatic filtering of archived, internal and linked agent records.
- Total and last completed model-response Input, Output and Cache tokens, with separate estimated USD costs.
- Live tokens/second, calculated from the preceding 60 seconds.
- Measured context usage and the capacity reported by the session.
- Five-hour and weekly account limits, reset timers and clearly marked approximate token equivalents when calibration is available.
- Model breakdown, subscription type and separate subagent consumption in Details.
- Tray integration, always-on-top, remembered window settings, transparency, dark/light themes and English/Turkish localization.
- Auto Follow Beta is off by default and preserves manual selection when the selected Desktop session cannot be verified.

### Download and install

The application is **free to use and closed-source**. Downloads are public and do not require a GitHub account or invitation. Application source code is not distributed in the downloads repository.

Open [Release 1.0 â†’ Assets](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases) and select your package:

| Platform | Package | Installation |
| --- | --- | --- |
| Windows x64 | `*_x64-setup.exe` | Run the installer, then open the app from the Start menu. |
| Windows x64 portable | `QufuCodexDashboard-1.0.exe` | Run the executable; WebView2 must be installed. |
| Ubuntu / Debian amd64 | `*_amd64.deb` | `sudo apt install ./downloaded-file.deb` |
| Linux x64 | `*_amd64.AppImage` | `chmod +x downloaded-file.AppImage`, then run it. |

Local Codex session records are required. Live account limits require a signed-in Codex CLI available as `codex` on PATH. The Windows installer detects WebView2 and automatically downloads/installs it when missing; this requires internet access. Installation stops if the runtime cannot be installed. Linux requires WebKitGTK 4.1 and a graphical session; GNOME may need an AppIndicator extension for the tray. Wayland can restrict window positioning and always-on-top behavior.

Before updating, use **Quit** in the tray menu to close the running app. Closing the window only hides it to the tray.

### Use and accuracy

The footer shows the last limit-update time and the age of stale data.

Select a workspace/session from the header. Open Details for model and subagent usage, or Settings for appearance and language. Defaults are English, 33% transparency and a 300 px compact window that fits its content. Preferences persist. Context warns above %80; account limits warn above %90.

Local metadata and logs are read without modification from `CODEX_HOME`, or `~/.codex`. Session discovery has no date cutoff or hard-coded names. Cache is included in Input and reasoning in Output; neither is added twice. Response IDs deduplicate usage, while main and linked-agent counters remain separate. Last request means the last completed model response, not an entire user turn.

Unknown values remain unavailable. USD is an API-equivalent estimate, not a subscription bill. The official [OpenAI pricing table](https://developers.openai.com/api/docs/pricing) is checked on every launch, with last-good cache and bundled first-launch fallback. Context uses measured usage and session-reported capacity, never a subscription-based guess.

Account percentages come from the installed Codex `account/rateLimits/read` interface. OpenAI does not report a fixed token allowance. Fractions marked `â‰ˆ` are estimated token equivalents from local price-weighted calibration, not official quotas or measured account-wide spending. Insufficient or unstable calibration remains unavailable; other devices and cloud use can affect accuracy. Cloud/ChatGPT conversations without local usage records are not listed. Auto Follow keeps manual selection when Desktop selection cannot be verified.

The app does not upload conversations or usage logs to a dashboard server and does not read authentication token files. Network activity is limited to public pricing requests, the installed Codex account reader, and GitHub update checks/downloads.

### Updates and license

Open Settings â†’ **Check for updates**. When a newer release is found, click **Download and install** to approve installation. The package signature and signed version are verified first. Windows may close during installation; Linux restarts the app afterward. The GitHub button opens the releases page. A failed network or missing release manifest is reported as a failed check, never as proof that the app is current.

Use is free. Application source, modification, redistribution and resale rights are not granted. See the [freeware license](LICENSE). Third-party components retain their own licenses.

## Author / Yazar

**[alper@qufu.io](mailto:alper@qufu.io)**

[qufu.io](https://qufu.io)

Copyright Â© 2026 alper@qufu.io. All rights reserved. The application is free to use under the [freeware license](LICENSE); its source code is not publicly distributed.

The in-app Qufu logo is supplied by the author. System icons use the approved Lucide Square Activity adaptation; see the [ISC license and attribution](docs/third-party/LUCIDE-LICENSE).
