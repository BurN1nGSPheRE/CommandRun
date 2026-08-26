# BurN1nGSPheRE — Pentest Command Cheatsheet (v2)

หน้าเว็บค้นหา command แบบ PWA (ใช้ offline ได้ / ติดตั้งลงมือถือได้)

## ไฟล์ในชุด (ต้องอยู่โฟลเดอร์เดียวกันทั้งหมด)
- `index.html` — หน้าเว็บหลัก (data-driven, 17 หมวด, 153 คำสั่ง)
- `manifest.json`, `sw.js` — PWA (ติดตั้ง + offline) — cache bump เป็น v2 แล้ว
- `icon-192.png`, `icon-512.png` — ไอคอนแอป

## ความสามารถใหม่
1. **แบ่งหมวด + คำอธิบายหมวด** — แต่ละหมวดมีข้อความบอกว่าใช้ทำอะไร (เช่น Ligolo pivot, AD ACL abuse, Windows privesc)
2. **Auto-fill ตัวแปร** — กรอก IP / DOMAIN / DC / USER / PASS / KALI IP / PORT / HASH ในกล่องบนสุด แล้วทุก command เติมค่าให้อัตโนมัติ กดที่ command เพื่อ copy ได้ทันที
   - เว้นว่าง = แสดงเป็น `<ip>` `<user>` ฯลฯ ให้ไปเติมเอง
   - token เฉพาะทางเช่น `<group>` `<winpath>` `<subnet>` เติมมือได้
   - ค่าที่กรอกถูกจำไว้ใน localStorage (เปิดใหม่ไม่ต้องกรอกซ้ำ)
3. **ปุ่ม `!` ท้ายทุก command** — กดแล้วเด้ง popup อธิบายแต่ละ flag/ส่วนของคำสั่งอย่างละเอียด (เช่น `evil-winrm -i` = ใส่ IP, `-u` = user, `-p` = password) และจะแสดงค่าจริงที่กรอกไว้ด้วย

## อัปโหลดขึ้น GitHub Pages
1. สร้าง repo public ที่ https://github.com/new
2. Add file → Upload files → ลากไฟล์ทั้ง 5 ใส่ → Commit
3. Settings → Pages → Deploy from branch → main → / (root) → Save
4. รอ 1-2 นาที ได้ URL `https://<username>.github.io/<repo>/`
5. iPhone/iPad: เปิดด้วย Safari → Share → Add to Home Screen

หมายเหตุ: เป็น cheatsheet ล้วน ไม่มี credential จริง — repo public ได้ไม่มีปัญหา
