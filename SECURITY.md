# Security Policy / Güvenlik Politikası

## Supported releases / Desteklenen sürümler

Security reports should target the latest published release of Qufu Codex Dashboard. Available fixes are distributed through new releases and signed in-app update packages. This policy does not promise a fixed response or remediation time.

Güvenlik bildirimleri Qufu Codex Dashboard'un yayınlanmış en güncel sürümünü hedeflemelidir. Hazır düzeltmeler yeni sürümler ve imzalı uygulama içi güncelleme paketleriyle dağıtılır. Sabit yanıt veya düzeltme süresi taahhüt edilmez.

## Report privately / Özel bildirim

Email **alper@qufu.io** with the subject **Qufu Codex Dashboard security report**. Include:

- Application version, operating system and installation method.
- A clear description, reproduction steps and potential impact.
- A minimal, sanitized proof of concept when necessary.

Do not disclose an unpatched vulnerability in public issues or PRs. Do not send authentication tokens, full Codex session logs or private conversations. Coordinate publication of technical details with the maintainer. If you do not receive a reply, follow up through the same email address.

**alper@qufu.io** adresine **Qufu Codex Dashboard security report** konusuyla e-posta gönder. Şunları belirt:

- Uygulama sürümü, işletim sistemi ve kurulum yöntemi.
- Açık açıklama, tekrar oluşturma adımları ve olası etki.
- Gerekliyse gizli verilerden arındırılmış, asgari bir örnek.

Henüz düzeltilmemiş açıkları public issue veya PR içinde paylaşma. Kimlik doğrulama tokenı, tüm Codex session logları veya özel konuşmalar gönderme. Teknik ayrıntıların yayınlanmasını proje sahibiyle koordine et. Yanıt alamazsan aynı e-posta üzerinden takip edebilirsin.

## Download integrity / İndirme bütünlüğü

Use the [official releases](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases). SHA256SUMS.txt accompanies each release. The in-app updater verifies package signatures and their signed version before installation. These updater signatures are distinct from operating-system code-signing certificates.

[Resmi sürümleri](https://github.com/qufu-io/qufu-codex-dashboard-releases/releases) kullan. Her sürümde SHA256SUMS.txt bulunur. Uygulama içi güncelleyici kurulum öncesinde paket imzasını ve imzalanmış sürümü doğrular. Bu imzalar işletim sisteminin kod imzalama sertifikalarıyla aynı şey değildir.
