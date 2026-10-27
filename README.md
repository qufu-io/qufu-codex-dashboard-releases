# Qufu Codex Dashboard

Understand your Codex usage in one compact desktop window. Track local sessions, complete tasks, API-equivalent costs and account limits — with a clear distinction between measured data and estimates.

[![Source checks](https://github.com/qufu-io/qufu-codex-dashboard/actions/workflows/ci.yml/badge.svg)](https://github.com/qufu-io/qufu-codex-dashboard/actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE) [![Latest release](https://img.shields.io/github/v/release/qufu-io/qufu-codex-dashboard-releases)](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases/latest)

**Open source · MIT · Version 1.0.2 · Windows & Linux · Author: [alper@qufu.io](mailto:alper@qufu.io)**

[Source](https://github.com/qufu-io/qufu-codex-dashboard) · [Contribute](CONTRIBUTING.md) · [Download 1.0.2](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases/tag/v1.0.2) · [Türkçe](#türkçe) · [English](#english) · [qufu.io](https://qufu.io)

<p align="center">
  <img src="docs/images/dashboard-1.0.png" width="300" alt="Qufu Codex Dashboard 1.0 showing session tokens, last request cost, context usage and account limits">
</p>

[What’s new / Yenilikler](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/docs/CHANGES-1.0.2.md) · [Changelog](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/CHANGELOG.md) · [Measurement methodology / Ölçüm yöntemi](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/docs/MEASUREMENTS.md) · [Privacy / Gizlilik](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/docs/PRIVACY.md)

| Measurement / Ölçüm | Source and meaning / Kaynak ve anlam |
| --- | --- |
| Tokens & Context | Official Codex measurements and CLI formulas / Resmî Codex ölçümleri ve CLI formülleri |
| Account limits | Official five-hour/weekly percentages / Resmî beş saatlik/haftalık yüzdeler |
| USD | Approximate API-equivalent cost; not your bill / Yaklaşık API eşdeğeri; fatura değildir |
| Quota capacity | Learned reference-token equivalent; not an official allowance / Öğrenilmiş referans token eşdeğeri; resmî kota değildir |

## Türkçe

Qufu Codex Dashboard, Codex kullanımını küçük bir masaüstü penceresinden takip etmeni sağlar. Tauri 2 ile geliştirilmiştir; Windows ve Linux üzerinde çalışır.

### Özellikler

- Workspace ve session seçimi; arşivlenmiş, internal ve subagent kayıtlarını ana listeden ayıran otomatik filtreleme.
- Session toplamı ve bir kullanıcı görev turunun tamamı için Input, Output, Cache tokenları ve tahmini USD maliyeti.
- Görev tüketimi, görev sonu context ve hesap genelindeki kota geçmişi için tıklayarak açılan küçük grafikler.
- Son 60 saniyeden hesaplanan canlı token/saniye değeri.
- Ölçülmüş context kullanımı ve session tarafından bildirilen context kapasitesi.
- 5 saatlik ve haftalık hesap limitleri, reset sayaçları ve veri yeterliyse açıkça işaretlenmiş tahmini token eşdeğerleri.
- Detaylar panelinde subagent tüketimi, model dökümü ve hesap abonelik türü.
- Her zaman üstte, sistem tepsisi, hatırlanan pencere ayarları, şeffaflık, koyu/açık tema ve Türkçe/İngilizce dil seçimi.
- Varsayılan kapalı Auto Follow Beta; seçili Desktop session doğrulanamıyorsa manuel seçimi korur.

### İndirme ve kurulum

Uygulama **ücretsiz ve MIT lisanslı açık kaynaklıdır**. [Kaynak kodunu](https://github.com/qufu-io/qufu-codex-dashboard) inceleyebilir, değiştirebilir ve lisans koşullarıyla paylaşabilirsin. İndirme için GitHub hesabı gerekmez.

1. [1.0.2 sürümünü aç](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases/tag/v1.0.2).
2. **Assets** bölümünü genişlet.
3. İşletim sistemine uygun paketi indir:

| Platform | Paket | Kurulum |
| --- | --- | --- |
| Windows x64 | `*_x64-setup.exe` | Dosyayı çalıştır; kurulumdan sonra Başlat menüsünden aç. |
| Windows x64, taşınabilir | `QufuCodexDashboard-1.0.2.exe` | Dosyayı çalıştır. WebView2 kurulu olmalı. |
| Ubuntu / Debian amd64 | `*_amd64.deb` | `sudo apt install ./indirilen-dosya.deb` |
| Linux x64 | `*_amd64.AppImage` | `chmod +x indirilen-dosya.AppImage` ardından dosyayı çalıştır. |

**Gereksinimler:** Yerel session verisi oluşturan Codex kurulumu. Canlı hesap limitleri için oturum açılmış Codex CLI (`codex` komutu PATH üzerinde) gerekir. Windows kurucusu WebView2'yi kontrol eder; eksikse internetten indirip otomatik kurar. WebView2 kurulumu başarısız olursa uygulama kurulumu durur. Linux'ta WebKitGTK 4.1 ve çalışan bir masaüstü oturumu gerekir; GNOME'da tray için AppIndicator eklentisi gerekebilir. Wayland, pencere konumunu ve her zaman üstte davranışını sınırlandırabilir.

**Güncelleme:** Eski uygulamayı tray menüsündeki **Quit / Çıkış** ile kapat, ardından yeni kurulumu çalıştır. Pencerenin X düğmesi uygulamayı tray'e gizler.

### Kullanım

Üstteki workspace/session adına tıklayıp takip edeceğin session'ı seç. Detaylar paneli model ve subagent dökümünü gösterir. Ayarlardan dil, tema, şeffaflık ve her zaman üstte seçeneklerini değiştirebilirsin.

Alt satır son limit güncelleme saatini gösterir; eski veride ne kadar süre geçtiği belirtilir.

Varsayılanlar: İngilizce, %33 şeffaflık, 300 piksel genişliğinde kompakt görünüm. Yükseklik içeriğe uyar; pencere ve sonraki tercihler hatırlanır. Context %80'i, hesap limitleri %90'ı aşınca ilgili bar ve yüzde uyarı rengine döner.

### Veriler ve hesaplama

- Yerel Codex metadata ve session kayıtları salt okunur kullanılır. `CODEX_HOME` ayarlıysa bu klasör, yoksa `~/.codex` okunur. Liste keşfinde tarih sınırı veya elle yazılmış session adları yoktur.
- Cache, Input'un; reasoning, Output'un alt kümesidir. Toplamda tekrar eklenmez. Ana session ve subagent tüketimleri ayrı sunulur.
- Bilinmeyen kullanım veya fiyat sıfır gösterilmez. Son istek bir **kullanıcı görev turunun tamamıdır**; devam eden, tamamlanan ve kesilen görevler ayrılır. Farklı modellerin USD maliyetleri yanıt bazında hesaplanır. CLI Used = Input − Cache + Output; Raw Total = Input + Output.
- USD tutarları API eşdeğeri tahmindir; abonelik faturası değildir. Resmi [OpenAI fiyatları](https://developers.openai.com/api/docs/pricing) her açılışta kontrol edilir; erişilemezse son geçerli fiyat, ilk açılışta ise dahil edilen fiyat tablosu kullanılır.
- Context miktarı ölçülmüş değerdir; yüzde, CLI’ın 12.000 token baseline düzeltmesi ve yuvarlamasıyla hesaplanır. Kapasite abonelikten tahmin edilmez.
- Hesap limitleri `account/rateLimits/read` üzerinden alınır. OpenAI sabit token kotası bildirmez. `≈` işaretli miktarlar, yerel token tüketimi ile limit yüzdesi değişiminden öğrenilen efektif kapasite tahminidir; resmi kota veya hesap genelinde ölçülmüş harcama değildir. Kapasite için yeterli/güvenilir veri yoksa doğrulanmış yerel tüketim korunur, kapasite bilinmiyor gösterilir. Başka cihaz ve bulut kullanımı tahminlerin doğruluğunu etkileyebilir.
- Kota kapasitesi sabit bir cache dışı input eşdeğerinde gösterilir. Beş saatlik N/C/O ağırlıkları gerçek gözlemlerden öğrenilir; haftalık hesap aynı ağırlıkları ve veriyle kalibre edilen bir oranı kullanır (ilk varsayım: 0,15). Yetersiz veri kesin kapasiteye dönüştürülmez. [Teknik yöntem ve sınırlar](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/docs/MEASUREMENTS.md).
- Yerel kullanım kaydı bulunmayan bulut/ChatGPT sohbetleri listelenmez. Auto Follow doğrulanmış Desktop seçimi bulunamazsa manuel kalır.

### Gizlilik ve paylaşım

Uygulama konuşmaları ve kullanım kayıtlarını bir dashboard sunucusuna yüklemez; kimlik doğrulama token dosyalarını okumaz. Ağ erişimi resmi fiyat kontrolü, kurulu Codex'in hesap limit okuyucusu ve GitHub güncelleme kontrolü/indirmesi içindir.

Ayarlar → **Güncellemeleri kontrol et** ile yeni sürümü sorgulayabilirsin. Yeni sürüm bulunduğunda **İndir ve kur** düğmesine tıklaman gerekir; kurulum kendiliğinden başlamaz. Paket imzası ve imzalanmış sürüm numarası doğrulanır. Windows kurulum sırasında kapanabilir; Linux'ta uygulama yeniden başlatılır. GitHub düğmesiyle tüm sürümleri tarayıcıda açabilirsin. İnternet veya yayın manifesti erişilemezse kontrol başarısız olarak gösterilir; uygulama güncelmiş gibi davranmaz.

Kaynak kodu ve projenin özgün varlıkları [MIT lisansı](LICENSE) altındadır. Üçüncü taraf bileşenlerin kendi lisansları korunur. [Lisans geçişi](docs/LICENSING.md), eski 1.0 kurulum paketlerinde görünen freeware metnini de açıklar.

## English

Qufu Codex Dashboard is a compact Tauri 2 desktop monitor for local Codex usage on Windows and Linux.

### Features

- Workspace/session picker with automatic filtering of archived, internal and linked agent records.
- Session totals and complete user-task Input, Output and Cache tokens, with separate API-equivalent costs.
- Small, click-to-open charts for task usage, measured end-of-task context and global quota history.
- Live tokens/second, calculated from the preceding 60 seconds.
- Measured context usage and the capacity reported by the session.
- Five-hour and weekly account limits, reset timers and clearly marked approximate token equivalents when calibration is available.
- Model breakdown, subscription type and separate subagent consumption in Details.
- Tray integration, always-on-top, remembered window settings, transparency, dark/light themes and English/Turkish localization.
- Auto Follow Beta is off by default and preserves manual selection when the selected Desktop session cannot be verified.

### Download and install

The application is **free and open source under MIT**. [Browse, modify and contribute to the source](https://github.com/qufu-io/qufu-codex-dashboard). Downloads are public and require no GitHub account.

Open [Release 1.0.2 → Assets](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases/tag/v1.0.2) and select your package:

| Platform | Package | Installation |
| --- | --- | --- |
| Windows x64 | `*_x64-setup.exe` | Run the installer, then open the app from the Start menu. |
| Windows x64 portable | `QufuCodexDashboard-1.0.2.exe` | Run the executable; WebView2 must be installed. |
| Ubuntu / Debian amd64 | `*_amd64.deb` | `sudo apt install ./downloaded-file.deb` |
| Linux x64 | `*_amd64.AppImage` | `chmod +x downloaded-file.AppImage`, then run it. |

Local Codex session records are required. Live account limits require a signed-in Codex CLI available as `codex` on PATH. The Windows installer detects WebView2 and automatically downloads/installs it when missing; this requires internet access. Installation stops if the runtime cannot be installed. Linux requires WebKitGTK 4.1 and a graphical session; GNOME may need an AppIndicator extension for the tray. Wayland can restrict window positioning and always-on-top behavior.

Before updating, use **Quit** in the tray menu to close the running app. Closing the window only hides it to the tray.

### Use and accuracy

The footer shows the last limit-update time and the age of stale data.

Select a workspace/session from the header. Open Details for model and subagent usage, or Settings for appearance and language. Defaults are English, 33% transparency and a 300 px compact window that fits its content. Preferences persist. Context warns above %80; account limits warn above %90.

Local metadata and logs are read without modification from `CODEX_HOME`, or `~/.codex`. Session discovery has no date cutoff or hard-coded names. Cache is included in Input and reasoning in Output; neither is added twice. Response IDs deduplicate usage, while main and linked-agent counters remain separate. Last request covers a complete user-task turn, with active, completed and interrupted states. Each response uses its own model/tier for USD. CLI Used = Input − Cache + Output; Raw Total = Input + Output. Known cost/agent subtotals remain visible when other records are missing; partial and approximate values are marked. Price lookup preserves service tiers and normalizes reasoning-effort aliases without treating effort as a separately billed model.

Unknown values remain unavailable. USD is an API-equivalent estimate, not a subscription bill. The official [OpenAI pricing table](https://developers.openai.com/api/docs/pricing) is checked on every launch, with last-good cache and bundled first-launch fallback. Context uses measured usage, session-reported capacity and the CLI’s 12,000-token baseline/rounding, never a subscription-based capacity guess.

Account percentages come from the installed Codex `account/rateLimits/read` interface. OpenAI does not report a fixed token allowance. Fractions marked `≈` are effective token capacities learned from local tokens and observed limit-percentage changes, not official quotas or measured account-wide spending. The initial ratio estimate transitions to positive robust ridge regression when sufficient observations exist. The five-hour model learns nonnegative N/C/O weights independently of API prices. Weekly capacity reuses these weights and a calibrated percentage ratio (initial assumption: 0.15). Both use a fixed uncached-input-equivalent reference unit, with empirical held-out errors in tooltips. See the [methodology and limitations](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/docs/MEASUREMENTS.md). Local SQLite observations survive restarts without a 14-day cutoff. Unstable calibration leaves capacity unavailable while preserving known local usage; other devices and cloud use can affect accuracy. Cloud/ChatGPT conversations without local usage records are not listed. Auto Follow keeps manual selection when Desktop selection cannot be verified.

The app does not upload conversations or usage logs to a dashboard server and does not read authentication token files. Network activity is limited to public pricing requests, the installed Codex account reader, and GitHub update checks/downloads.

### Updates and license

Open Settings → **Check for updates**. When a newer release is found, click **Download and install** to approve installation. The package signature and signed version are verified first. Windows may close during installation; Linux restarts the app afterward. The GitHub button opens the releases page. A failed network or missing release manifest is reported as a failed check, never as proof that the app is current.

The source and original project assets are available under the [MIT license](LICENSE). Third-party components retain their own licenses. See the [license transition](docs/LICENSING.md) for the legacy freeware wording still embedded in previously published 1.0 installers.

## Source and contributions / Kaynak kodu ve katkılar

This repository hosts official downloads and release documentation. Source code, tests and build instructions live in the [MIT source repository](https://github.com/qufu-io/qufu-codex-dashboard). Read the [development guide](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/docs/DEVELOPMENT.md) to build or contribute.

Bu depo resmî indirmeleri ve sürüm belgelerini içerir. Kaynak kodu, testler ve derleme yönergeleri [MIT kaynak deposundadır](https://github.com/qufu-io/qufu-codex-dashboard). Katkı ve derleme için [geliştirme rehberini](https://github.com/qufu-io/qufu-codex-dashboard/blob/v1.0.2/docs/DEVELOPMENT.md) kullan.

## Community / Topluluk

- [Contribution guide / Katkı rehberi](CONTRIBUTING.md)
- [Code of Conduct / Davranış kuralları](CODE_OF_CONDUCT.md)
- [Security policy / Güvenlik politikası](SECURITY.md)
- [Bug reports and feature requests / Hata ve özellik önerileri](https://github.com/qufu-io/qufu-codex-dashboard/issues/new/choose)

## Contributors / Katkıda bulunanlar

| Contributor / Katkıda bulunan | Role / Rol |
| --- | --- |
| [qufu-io](https://github.com/qufu-io) — [alper@qufu.io](mailto:alper@qufu.io) | Project owner and developer / Proje sahibi ve geliştirici |
| [OpenAI Codex](https://github.com/codex) | AI development assistant / Yapay zekâ geliştirme asistanı |

Development commits credit [qufu-io](https://github.com/qufu-io) as author and [Codex](https://github.com/codex) as AI co-author. / Geliştirme commitlerinde qufu-io yazar, Codex ise yapay zekâ ortak yazar olarak belirtilir.

## Author / Yazar

**[alper@qufu.io](mailto:alper@qufu.io)**

[qufu.io](https://qufu.io)

Copyright © 2026 alper@qufu.io. Licensed under [MIT](LICENSE). This is an independent community project, not an official OpenAI product or endorsement.

The in-app Qufu logo is supplied by the author. System icons use the approved Lucide Square Activity adaptation; see the [ISC license and attribution](docs/third-party/LUCIDE-LICENSE).
