

Quyidagi diagram `signer.py` faylining ish jarayonini blok-sxema tarzida ko‘rsatadi:

```mermaid
graph TD
    A[Start] --> B[private.pem faylini ochish]
    B --> C[Xususiy kalitni yuklash]
    C --> D[Xabar tayyorlash: "Durdona Shermuhammadova Anvar qizi"]
    D --> E[Imzo yaratish (RSA-PSS + SHA256)]
    E --> F[Imzoni Base64 formatiga o'tkazish]
    F --> G[Xabar va Imzoni chiqarish]
    G --> H[End]
```mermaid
graph TD
    A[Start] --> B[Ochiq kalitni ochish]
    B --> C[Xabar tayyorlash: "Durdona S."]
    C --> D[Base64 imzoni kiritish]
    D --> E[Imzoni dekodlash]
    E --> F[Imzoni tekshirish (RSA-PSS + SHA256)]
    F --> G{Natija?}
    G -->|To‘g‘ri| H[✔️ Imzo to‘g‘ri!]
    G -->|Noto‘g‘ri| I[❌ Imzo noto‘g‘ri!]
    H --> J[End]
    I --> J
