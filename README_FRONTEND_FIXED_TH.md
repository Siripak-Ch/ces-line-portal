# CES Hub GitHub Frontend Fixed

ชุดนี้แก้เฉพาะฝั่ง GitHub frontend โดยอ้างอิง backend Apps Script จาก `download(14).zip` และ stock UI snippets ที่แนบมา

## Sheet IDs ที่ต้องตรงกับ backend health
- Main: `1w3_j_2T67f9xy_ndGYw9LuuKCPEttw52zwVUxM1zUNE`
- KPI: `1vNt7qUenxteIV3A0TnQ2QYf0esyOu3NvEjZG8zme5Gk`
- Stock: `1X7f6BatQ-y5ZW6VYTv2oT34rbsCLeNgac0APt7njFrk`

## Files changed
- `js/config.js` — เพิ่ม expected sheet IDs และตั้งค่า API endpoint
- `js/gas-polyfill.js` — bridge ใหม่ รองรับ JSONP GET + hidden iframe POST
- `index.html` — update Stock Dashboard / Inventory / Check Stock HTML section จากไฟล์ล่าสุดที่แนบ และแสดง error message ชัดขึ้น
- `api-test-all.html` — หน้า test API ทุก module

## วิธีใช้
1. วางไฟล์ทั้งหมดใน root repo `ces-line-portal`
2. แก้ `js/config.js` ให้ `GAS_API_URL` เป็น Apps Script `/exec` ล่าสุด ถ้า URL เปลี่ยน
3. Push GitHub Pages
4. เปิด `/api-test-all.html` แล้วกด `Run Core`, `Run Read Modules`, `Run Stock`
5. ถ้าผ่านแล้วค่อยเปิด `/index.html`

## สำคัญ
ถ้า API test ขึ้น sheet ID ไม่ตรง ให้แก้ backend Apps Script ไม่ใช่ frontend
