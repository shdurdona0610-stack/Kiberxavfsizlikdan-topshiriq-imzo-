Imzoni yaratish blok sxemasi 
```mermaid
graph TD
    A1[Start] --> B1[private.pem ochish]
    B1 --> C1[Xususiy kalit tayyorlash]
    C1 --> D1[Xabar tayyorlash]
    D1 --> E1[Imzo yaratish (RSA-PSS + SHA256)]
    E1 --> F1[Imzoni Base64 ga o'tkazish]
    F1 --> G1[Natijani chiqarish]
    G1 --> H1[End]
```

