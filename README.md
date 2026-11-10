# Number Studio Premium · PWA Demo

เว็บแอปต้นแบบสำหรับการบันทึกเลขและวงเงิน **จำลอง** 2 ตัวและ 3 ตัว พร้อมรายงานยอดสะสมและจำนวนรายการตามเลข รองรับหน้าบ้าน หลังบ้าน และรายงาน และติดตั้งบนหน้าจอหลักมือถือได้

## ติดตั้ง GitHub Pages

1. แตก ZIP แล้วอัปโหลด `index.html`, `manifest.webmanifest`, `service-worker.js` และโฟลเดอร์ `icons` ไปที่ root ของ repository (คงโครงสร้างเดิม)
2. เปิด Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save
3. เปิด URL GitHub Pages ผ่าน HTTPS บนมือถือ จากนั้นบน Android ใช้เมนู Install app / Add to Home Screen; บน iPhone ใช้ Share → Add to Home Screen

## ข้อจำกัด

- รายการถูกเก็บด้วย localStorage ของเบราว์เซอร์แต่ละเครื่อง: ไม่ซิงก์ระหว่างมือถือ/คอมพิวเตอร์
- Service worker แคชหน้าแอปไว้เพื่อเปิดใช้งานซ้ำแบบออฟไลน์หลังเข้าชมครั้งแรก แต่ฟอนต์จาก Google อาจใช้ฟอนต์สำรองเมื่อออฟไลน์
- การติดตั้ง PWA ต้องใช้ HTTPS หรือ localhost; เปิด `index.html` ผ่าน file:// จะไม่ลงทะเบียน service worker
- ไม่มีการล็อกอินหรือการรับชำระเงินหรือธุรกรรมซื้อขายจริง
- หากอัปเดตโค้ดในอนาคตให้เปลี่ยนชื่อ CACHE ใน service-worker.js เพื่อรีเฟรชแคช
