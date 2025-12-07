# Kiberxavfsizlikdan-topshiriq-imzo-
``` mermaid
flowchart TD
    A[Boshlash] --> B[Kutubxonalarni import qilish]
    B --> C[Xususiy kalitni o'qish ("private.pem")]
    C --> D[Xabar tayyorlash<br>message = b"Durdona Shermuhammadova Anvar qizi"]
    D --> E[Imzo yaratish<br>RSA-PSS + SHA256]
    E --> F[Xabar va imzoni chiqarish<br>print(message)<br>print(signature Base64)]
    F --> G[Tugatish]
