# Frontend Patch Notes

แก้ไข upload Excel ใน Service CSI และ Report CSI:
- ตรวจไฟล์ว่างก่อน mapping
- เพิ่ม `withFailureHandler()` เพื่อไม่ให้ loading overlay ค้าง
- Revenue default year fix เป็น 2026

ตรวจ `js/config.js` ให้ `GAS_API_URL` เป็น Apps Script deployment `/exec` ล่าสุดทุกครั้งหลัง redeploy backend
