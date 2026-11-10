# BiDiWhisper downloads

Windows için yerel sesli dikte, Türkçe metin düzeltme ve Türkçe–İngilizce çift yönlü çeviri.

**[Windows x64 kurulumunu indir — v0.3.0, 253 MB](https://github.com/halilozturkci/BiDiWhisper-releases/releases/download/v0.3.0/BiDiWhisper_0.3.0_x64-setup.exe)**

[Sürüm notları ve dosyalar](https://github.com/halilozturkci/BiDiWhisper-releases/releases/tag/v0.3.0) · [SHA-256 kontrol toplamı](https://github.com/halilozturkci/BiDiWhisper-releases/releases/download/v0.3.0/SHA256SUMS.txt)

Bu depo dağıtım bilgilerini ve lisans bildirimlerini içerir. Uygulamanın kaynak deposu private olarak tutulur. İndirmek için GitHub hesabı gerekmez.

## Kurulum

1. Yukarıdaki kurulum dosyasını indirin ve çalıştırın. Normal kullanıcı kurulumu veya taşınabilir kurulum seçilebilir.
2. İlk açılışta Whisper modelini indirin. Otomatik düzeltme veya çeviri kullanmak için **Yerel metin** bölümünden Qwen modelini indirin veya uyumlu GGUF dosyasını içe aktarın.
3. Tray menüsünden çıktı modunu ve Windows ile başlama tercihlerini ayarlayın. Kısayol uygulamanın Genel ayarlarında gösterilir ve değiştirilebilir.

İlk model indirmesi internet gerektirir: Whisper large-v3-turbo Q8 yaklaşık 886 MB, isteğe bağlı Qwen3.5-4B Q4_K_M yaklaşık 2,74 GB. Modeller kurulum dosyasına dahil değildir. Kurulu modellerle dikte, düzeltme ve çeviri cihaz üzerinde çalışır. Rust, Python, Bun veya ayrı bir model sunucusu kurulumu gerekmez; çalışma bileşenleri ve WebView2 çevrimdışı yükleyicisi pakettedir.

## Kullanım

- **Ham dikte:** yalnızca konuşma tanıma; en hızlı mevcut çıktı modu.
- **Türkçe düzeltme:** konuşma tanımadan sonra yerel metin düzeltme.
- **Türkçe → İngilizce / İngilizce → Türkçe:** yerel çeviri. Modelin çevirisi aynen aktarılır; hataları kullanıcı düzenler.
- **Modeli belleğe yükle:** Qwen'in ilk yükleme süresini konuşmadan önce tamamlar; model bellekte kalır.

Windows tray simgesini gizliyorsa **Ayarlar → Kişiselleştirme → Görev çubuğu → Diğer sistem tepsisi simgeleri → BiDiWhisper** seçeneğini açın. Pencereyi kapatmak, tray açıkken uygulamayı arka planda bırakır. Mikrofon kayıt komutuyla açılır.

## Sürüm durumu

v0.3.0 bir **imzasız Windows x64 test sürümüdür**. Dikte/çeviri hataları olabilir; özellikle İngilizce→Türkçe koşullu cümlelerde anlam hataları görülmüştür. Temiz Windows kurulumunda WebView2'nin bulunmadığı senaryo henüz doğrulanmadı. macOS ve Windows ARM64 paketi bu sürümde yoktur.

İndirilen dosyanın SHA-256 değerini sürümdeki `SHA256SUMS.txt` ile karşılaştırabilirsiniz. Paket 147 dosya kontrolünden, kurulu bileşenlerle ses tanıma ve Qwen çeviri testlerinden geçti; bu testler genel doğruluk veya her donanımda aynı hız garantisi değildir.

## Licenses / English

BiDiWhisper is an independent desktop application derived from [Handy](https://github.com/cjpais/Handy). This repository distributes Windows installers and notices; application source is maintained privately. Model downloads require internet initially; inference uses local files afterwards. The current Windows x64 release is an unsigned preview.

Preserve [LICENSE](LICENSE) and [third-party notices](THIRD-PARTY-NOTICES.md) when redistributing the package. Model licenses and Microsoft runtime terms remain applicable to their respective components.
