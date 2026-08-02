# BurN1nGSPheRE — วิธีอัปโหลดขึ้น GitHub Pages (ฟรี)

## ไฟล์ในชุดนี้
- `index.html` — หน้าเว็บหลัก (เพิ่ม PWA meta tags แล้ว)
- `manifest.json` — บอก iOS/Android ว่านี่คือ "แอป" ชื่ออะไร ไอคอนอะไร
- `sw.js` — Service Worker ทำให้เปิดใช้งาน offline ได้หลังโหลดครั้งแรก
- `icon-192.png`, `icon-512.png` — ไอคอนแอป (ธีมสีเดียวกับตัวเว็บ)

**ทั้ง 5 ไฟล์ต้องอยู่โฟลเดอร์เดียวกัน (root) ห้ามแยกโฟลเดอร์**

## ขั้นตอน

### 1. สร้าง Repository บน GitHub
1. ไปที่ https://github.com/new
2. ตั้งชื่อ repo เช่น `burn1ngsphere`
3. เลือก **Public**
4. กด **Create repository**

### 2. อัปโหลดไฟล์ทั้งหมด
1. ในหน้า repo ที่เพิ่งสร้าง กด **Add file → Upload files**
2. ลากไฟล์ทั้ง 5 ไฟล์ (`index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`) ใส่เข้าไปพร้อมกัน
3. กด **Commit changes**

### 3. เปิดใช้งาน GitHub Pages
1. ไปที่ **Settings** (แท็บบนสุดของ repo) → เมนูซ้าย **Pages**
2. หัวข้อ **Build and deployment** → Source เลือก **Deploy from a branch**
3. Branch เลือก **main**, folder เลือก **/ (root)** → กด **Save**
4. รอ 1–2 นาที จะได้ URL แบบ:
   `https://<username>.github.io/burn1ngsphere/`

### 4. ติดตั้งลง iPhone/iPad
1. เปิด URL ด้านบนด้วย **Safari** (ต้องเป็น Safari เท่านั้น ใช้ Chrome ไม่ได้)
2. กดปุ่ม **Share** (สี่เหลี่ยมมีลูกศรชี้ขึ้น)
3. เลื่อนหาแล้วกด **Add to Home Screen**
4. ตั้งชื่อ (หรือใช้ค่า default "BurN1nG") → กด **Add**

จะได้ไอคอนหน้าจอ Home Screen เปิดแบบ full screen ไม่มี address bar, ใช้งาน offline ได้หลังเปิดครั้งแรก (จาก Service Worker cache)

## หมายเหตุ
- ถ้าแก้ไขเนื้อหาในอนาคต ให้แก้ `index.html` แล้วอัปโหลดทับ (Add file → Upload files → เลือกไฟล์เดิม) — GitHub Pages จะอัปเดตให้อัตโนมัติใน 1-2 นาที
- ถ้าต้องการเปลี่ยนไอคอน ให้แทนที่ `icon-192.png` และ `icon-512.png` ด้วยไฟล์ขนาดเดียวกัน (พื้นหลังสี่เหลี่ยมจัตุรัส)
- repo เป็น Public หมายความว่าใครก็เข้าดูโค้ดได้ (แต่นี่คือ cheatsheet ไม่ใช่ข้อมูลลับ credential ใดๆ ก็ไม่มีปัญหา)
