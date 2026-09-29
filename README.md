# หารบิล — ตัวอย่าง web app บน Vercel

```
bill-splitter/
├── index.html      # หน้าเว็บ (HTML + CSS + JS)
├── api/hello.js    # Serverless function → /api/hello
└── package.json
```

## วิธีที่ 1: ผ่าน GitHub (แนะนำ — push แล้ว deploy ใหม่อัตโนมัติ)
1. สร้าง repo ใหม่บน GitHub แล้วอัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้
2. เข้า https://vercel.com → Sign up ด้วยบัญชี GitHub
3. กด **Add New… → Project** → เลือก repo → **Deploy**
4. ได้ลิงก์ `https://<ชื่อ>.vercel.app` ทุกครั้งที่ push จะ deploy ให้เอง

## วิธีที่ 2: ผ่าน Vercel CLI (เร็วที่สุด)
ต้องมี Node.js ในเครื่อง
```bash
cd bill-splitter
npx vercel          # ครั้งแรกจะให้ login และถามค่าตั้งต้น กด Enter ได้เลย
npx vercel --prod   # deploy ขึ้น production
```

## ทดสอบในเครื่อง
```bash
npx vercel dev      # เปิด http://localhost:3000
```
