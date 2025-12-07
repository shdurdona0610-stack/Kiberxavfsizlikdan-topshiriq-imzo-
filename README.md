

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
