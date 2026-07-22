> **Project Status: Inactive**
>
> This repository is no longer actively maintained and is being preserved for educational or historical reference.

# Stellar ve Soroban ile Akıllı Sözleşme Bağış Projesi

Bu proje, [Stellar](https://www.stellar.org/) ağı üzerinde [Soroban](https://developers.stellar.org/docs/build/smart-contracts) akıllı sözleşmeleri kullanılarak oluşturulmuş basit bir bağış platformu örneğidir.

Projenin temel amacı, belirli bir amaç için (örneğin, açık kaynaklı bir projeye destek) on-chain (zincir üzerinde) bağış toplanmasını sağlayan ve toplanan toplam miktarı şeffaf bir şekilde gösteren bir akıllı sözleşme oluşturmaktır.

## 🚀 Proje Hakkında

Bu repo, iki ana bileşenden oluşur:

1.  **Akıllı Sözleşme (`/contract`):** Rust dilinde yazılmış ve Soroban platformunda çalışan akıllı sözleşme. Bu sözleşme, XLM (veya başka bir Stellar tokeni) kabul eder, toplanan toplam bağış miktarını kendi depolama alanında (state) tutar ve bu miktarı sorgulayan bir fonksiyon sunar.
2.  **Frontend Arayüzü (`/frontend`):** Kullanıcıların bağış yapmasını sağlayan bir "Baİış Butonu" ve sözleşmeden alınan veriyi gösteren basit bir web arayüzü (HTML/JS/CSS).

## 🛠️ Kullanılan Teknolojiler

* **Stellar:** Hızlı ve düşük maliyetli işlemler için kullanılan blockchain ağı.
* **Soroban:** Stellar üzerinde akıllı sözleşmeler yazmak için kullanılan platform.
* **Rust:** Akıllı sözleşmeyi yazmak için kullanılan programlama dili.
* **Stellar SDK (JavaScript):** Frontend'in kullanıcının cüzdanı (Freighter gibi) ile ve akıllı sözleşme ile etkileşime girmesi için kullanılır.

## 📂 Proje Yapısı
```bash
├──  kontrakt/           # Akıllı sözleşme Rust projesi
│   ├── Cargo.toml
│   └── src/
│       └── lib.rs      # Ana sözleşme kodu (donate, get_total vb.)
│
├── frontend/           # Web arayüzü
│   ├── index.html
│   ├── app.js          # Sözleşme ile etkileşim kodu
│   └── style.css
│
├── .gitignore
└── README.md           # Bu dosya
```