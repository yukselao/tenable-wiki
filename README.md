# Tenable Wiki

Tenable ekosistemi için kurulum, operasyon ve mimari notlarının yaşayan
derlemesi. [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) ile
inşa edilir, GitHub Pages üzerinden yayınlanır.

> **Site**: https://yukselao.github.io/tenable-wiki/

## İçindekiler

- **OpenShift**
  - [Managed Nessus Scanner Kurulumu](docs/openshift/nessus-scanner.md) — online ve offline kurulum, SCC çözümü, otomasyon scripti

## Yerel önizleme

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
# http://127.0.0.1:8000
```

## Yapı

```
.
├── mkdocs.yml                  # Site konfigürasyonu
├── requirements.txt            # Python bağımlılıkları
├── docs/                       # Markdown içerik
│   ├── index.md                # Anasayfa
│   └── openshift/
│       ├── index.md
│       └── nessus-scanner.md
├── assets/
│   └── samples/                # Manifest'ler, örnek dosyalar
│       └── nessus-scanner-deployment.yaml
└── .github/workflows/deploy.yml  # GitHub Pages otomatik deploy
```

## GitHub Pages'ı aktif etme (tek seferlik)

1. Repo → **Settings** → **Pages**
2. **Source** → **GitHub Actions**

`main` branch'e her push'ta `.github/workflows/deploy.yml` site'ı yeniden inşa
edip yayınlar.

## Katkı

Düzeltme veya yeni içerik için PR aç; hatalı/eksik bilgileri issue olarak
raporla.
