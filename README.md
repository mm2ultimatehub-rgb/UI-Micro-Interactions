# UI Mikro-Etkileşim Galerisi

Saf HTML, CSS ve JavaScript ile hazırlanmış, GitHub Pages üzerinde doğrudan yayınlanabilen mikro-etkileşim koleksiyonu.

## Özellikler
- Derleme veya sunucu gerektirmeyen statik galeri
- Katalog yalnızca `components.json` üzerinden yönetilir
- Tembel yüklenen iframe canlı önizlemeleri
- Tam ekran önizleme ve mobil/masaüstü görünümü
- Kod kopyalama, dosya indirme, arama ve etiket filtreleri
- Koyu buzlu cam tasarım ve responsive düzen

## Yeni bileşen ekleme
1. `components/` içine bağımsız HTML dosyası ekleyin.
2. `components.json` içine `id`, `name`, `file`, `description`, `tags` alanlarıyla nesne ekleyin.
3. Dosya adı ile `file` alanını eşleştirin.

## GitHub Pages
1. **Settings → Pages** bölümünü açın.
2. **Deploy from a branch** seçin.
3. Branch: **main**, folder: **/(root)** seçip kaydedin.
4. Yayın URL'si birkaç dakika içinde görünür.

## Lisans
MIT — ayrıntılar için [LICENSE](LICENSE).
