---
hide:
  - navigation
  - toc
---

# Tenable Wiki

<div class="author-card">
  <img src="assets/avatar.png" alt="Ali Okan Yüksel" class="author-avatar" />
  <div class="author-meta">
    <span class="author-name">Ali Okan Yüksel</span>
    <span class="author-role">Yazar</span>
  </div>
</div>

Tenable ekosistemi kurulum, operasyon ve mimari notlarının yaşayan derlemesi.
Yayınladığımız içerikler saha tecrübelerine dayanan, doğrulanmış adımları içerir.

<div class="grid cards" markdown>

-   :material-kubernetes:{ .lg .middle } **Managed Nessus Scanner Deployment on Red Hat OpenShift**

    ---

    SC tarafından yönetilen Nessus scanner'ın OpenShift / CRC üzerinde online ve offline (air-gapped) kurulumu, SCC `anyuid` çözümü, otomasyon scripti.

    [:octicons-arrow-right-24: Dökümanı aç](openshift/nessus-scanner.md)

-   :material-restore-alert:{ .lg .middle } **Lisans Kaynaklı Erişim Sorunlarında Nessus'u Fabrika Ayarlarına Sıfırlama**

    ---

    Lisans sorunu nedeniyle web arayüzüne erişilemediğinde Nessus'u fabrika ayarlarına döndüren `nessuscli fix` komutları ve sıfırlama sonrası lisans kayıt akışı.

    [:octicons-arrow-right-24: Dökümanı aç](nessus/factory-reset.md)

-   :material-chart-line:{ .lg .middle } **Akıllı Önceliklendirme: VPR, ACR ve AES Skorlarının Birlikte Çalışma Matematiği**

    ---

    VPR (dinamik tehdit), ACR (varlık kritikliği) ve AES (toplam maruziyet) üçlüsünün birbirini nasıl beslediği, %60 → %1.6 gürültü filtresi, APA boyutu ve 1 Temmuz 2026 VPR v2 geçişi.

    [:octicons-arrow-right-24: Dökümanı aç](tenable-one/onceliklendirme-skorlari/index.md)

</div>

## Bu wiki nasıl kullanılır?

- Sol üstteki sekmelerden ana bölüme, soldaki menüden alt sayfalara erişebilirsin.
- Sağ üstteki :material-magnify: ile içerikte arama yapabilirsin (Türkçe + İngilizce).
- Her sayfada sağ üstteki :material-pencil: ikonu seni GitHub üzerinde dosyayı düzenleme ekranına götürür.
- Kod blokları üzerine geldiğinde sağdaki :material-content-copy: ile tek tıkla kopyalayabilirsin.

## Katkı

Bu wiki açık kaynaktır. Düzeltme veya yeni içerik için pull request açabilir,
hatalı/eksik bilgiyi issue olarak raporlayabilirsin:
[github.com/yukselao/tenable-wiki](https://github.com/yukselao/tenable-wiki).
