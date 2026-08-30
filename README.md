# WolfROYAL Discord Yönetim Paneli

Videodaki mobil yönetim panelinin aynı görsel dilini ve ana ekranlarını temel alan, gerçek Discord.js v14 + MongoDB entegrasyonuna hazır full-stack proje.

## Gereksinimler
- Node.js 20+ (22 önerilir)
- MongoDB 7/8 (lokal veya Atlas)
- Discord bot tokenı
- Discord Developer Portal'dan OAuth2 bilgileri (OAuth akışı sonraki entegrasyon noktası olarak ayrılmıştır)

## Kurulum
```bash
npm install
cd server && copy .env.example .env
```
`.env` içindeki `MONGODB_URI` ve `DISCORD_TOKEN` değerlerini doldur.

Sonra:
```bash
cd ..
npm run dev
```
Panel: http://localhost:5173
API: http://localhost:3001/api/health

Üretim:
```bash
npm run build
npm start
```

## Discord bot izinleri
Botu sunucuya eklerken gerekli olduğunda `ManageGuild`, `ManageRoles`, `ManageChannels`, `ModerateMembers`, `KickMembers`, `BanMembers`, `ViewAuditLog`, `ManageWebhooks`, `ManageMessages`, `ReadMessageHistory`, `SendMessages`, `Connect`, `Speak` izinlerini verin. Bot rolünü yönetmesi gereken rollerin üstüne taşıyın.

## Not
Gerçek Discord OAuth2 için Client ID/Secret ve callback URL'si sunucu tarafında saklanmalıdır; secret değerlerini frontend'e koymayın. Paneldeki demo sunucu verileri gerçek bot bağlandığında API uçlarına bağlanabilir.
