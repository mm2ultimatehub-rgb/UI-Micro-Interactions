# UI Mikro-Etkileşim Galerisi

Saf HTML, CSS ve JavaScript ile hazırlanmış; GitHub Pages üzerinde yayınlanabilen mikro-etkileşim koleksiyonu ve herkese açık topluluk galerisi.

## Özellikler
- Derleme veya kendi sunucunu gerektirmeyen statik galeri
- Katalog yalnızca `components.json` üzerinden yönetilir
- Tembel yüklenen iframe canlı önizlemeleri
- Tam ekran önizleme ve mobil/masaüstü görünümü
- Kod kopyalama, dosya indirme, arama ve etiket filtreleri
- Supabase Auth ile kullanıcı kaydı ve oturum
- Kullanıcı adı + e-posta + şifre ile kayıt; kullanıcı adı + şifre ile giriş
- Herkese açık gönderiler, profil adı ve gönderi sahibine özel silme yetkisi
- PNG/JPG/WEBP/GIF, SVG, ZIP, PDF ve kod/metin dosyası yükleme (dosya başına 25 MB)
- Kullanıcı HTML/JS dosyaları ana galeri içinde çalıştırılmaz; güvenli şekilde indirme bağlantısı olarak sunulur

## Topluluk altyapısı

Bu proje Supabase projesi `vyra-community` ile bağlıdır. Veritabanı tabloları, RLS politikaları, herkese açık dosya kovası ve `username-login` Edge Function kuruldu.

### İlk yayın öncesi Supabase ayarı
1. Supabase Dashboard'da **Authentication → URL Configuration** sayfasını aç.
2. **Site URL** değerini `https://mm2ultimatehub-rgb.github.io/UI-Micro-Interactions/` yap.
3. Aynı adresi **Redirect URLs** listesine ekle.
4. **Authentication → Providers → Email** bölümünde e-posta doğrulama ayarını kontrol et. Doğrulama açıksa kullanıcılar kayıt sonrası e-postalarındaki bağlantıya tıklamalı.
5. Supabase **Edge Functions** bölümünde `username-login` fonksiyonunun aktif olduğunu doğrula.

Supabase istemci anahtarı tarayıcıda kullanıldığı için publishable anahtar olarak tasarlanmıştır. **Service role / secret key hiçbir zaman GitHub deposuna veya tarayıcı koduna eklenmemelidir.** Veritabanı erişimi RLS politikalarıyla sınırlandırılır.

### Dosya güvenliği
- Topluluk gönderileri herkese açıktır; gönderiyi yalnızca sahibi silebilir.
- Kullanıcı e-postaları herkese açık profil tablosunda tutulmaz.
- HTML, JavaScript ve SVG içerikleri ana galeriye gömülerek çalıştırılmaz. Bilinmeyen dosyaları indirirken dikkatli olun.
- Dosya yükleme sınırı dosya başına 25 MB'dır.

## Yeni bileşen ekleme
1. `components/` içine bağımsız HTML dosyası ekleyin.
2. `components.json` içine `id`, `name`, `file`, `description`, `tags` alanlarıyla nesne ekleyin.
3. Dosya adı ile `file` alanını eşleştirin.

## GitHub Pages
1. **Settings → Pages** bölümünü açın.
2. **Deploy from a branch** seçin.
3. Branch: **main**, folder: **/(root)** seçip kaydedin.
4. Yayın URL'si: https://mm2ultimatehub-rgb.github.io/UI-Micro-Interactions/

## Lisans
MIT — ayrıntılar için [LICENSE](LICENSE).
