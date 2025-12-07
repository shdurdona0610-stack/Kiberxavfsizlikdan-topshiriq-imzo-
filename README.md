

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
    A[Start] --> B[public.pem faylini ochish]
    B --> C[Ochiq kalitni yuklash]
    C --> D[Xabar tayyorlash: "Durdona Shermuhammadova Anvar qizi"]
    D --> E[Base64 formatidagi imzoni kiritish]
    E --> F[Imzoni Base64 dan dekodlash]
    F --> G[Imzoni tekshirish (RSA-PSS + SHA256)]
    G --> H{Tekshirish natijasi?}
    H -->|To‘g‘ri| I[✔️ Imzo to‘g‘ri!]
    H -->|Noto‘g‘ri| J[❌ Imzo noto‘g‘ri!]
    I --> K[End]
    J --> K
