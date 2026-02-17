# Deriv Trading Chart with WebGPU Indicators

## ไฟล์ทั้งหมด
- `index.html` - หน้าเว็บหลัก
- `deriv-api.js` - Class สำหรับเชื่อมต่อ Deriv API
- `webgpu-indicators.js` - Class คำนวณ indicators ด้วย GPU
- `chart-manager.js` - Class จัดการ Lightweight Charts
- `app.js` - Application หลัก

## วิธีใช้งาน

### 1. เปิดไฟล์ index.html ใน Browser
- ใช้ Chrome, Edge, หรือ Firefox (รุ่นใหม่)
- รองรับ GPU acceleration (ถ้ามี)

### 2. ฟีเจอร์ที่มี
- ✅ ดึงข้อมูล Historical จาก Deriv
- ✅ รับข้อมูล Live Candles แบบ Real-time
- ✅ วาดกราฟด้วย Lightweight Charts 4.2.1
- ✅ คำนวณ MA 3 เส้น (SMA, EMA, HMA)
- ✅ กราฟ RSI
- ✅ กราฟ Choppiness Index
- ✅ Timeframe: 1M, 3M, 15M, 30M
- ✅ ใช้ GPU.js คำนวณ (GPU/CPU mode)
- ✅ แสดงสถานะ GPU/CPU

### 3. การใช้งาน
1. เลือก Symbol (Volatility Index หรือ Forex)
2. เลือก Timeframe
3. คลิก "Load History" เพื่อดึงข้อมูล
4. คลิก "Start Live" เพื่อรับข้อมูล real-time
5. ปรับ MA Type และ Period ตามต้องการ
6. คลิก "Update Indicators" เพื่ออัพเดท

### 4. การใช้ Class ในโปรเจคอื่น

```javascript
// ใช้ DerivAPI
const api = new DerivAPI('YOUR_APP_ID');
await api.connect();
const candles = await api.getHistoricalCandles('R_10', 60, 1000);

// ใช้ WebGPUIndicators
const indicators = new WebGPUIndicators();
const ema = indicators.calculateEMA(prices, 20);
const rsi = indicators.calculateRSI(prices, 14);
const status = indicators.getGPUStatus(); // ตรวจสอบสถานะ GPU

// ใช้ ChartManager
const charts = new ChartManager();
charts.updateCandles(candlesData);
charts.updateMA(0, maData);
```

### 5. GPU Status
- 🟢 **GPU Accelerated** - ใช้ GPU คำนวณ (เร็วกว่า)
- 🟠 **CPU Mode** - ใช้ CPU คำนวณ (ช้ากว่า)

## ข้อกำหนดระบบ
- Browser รุ่นใหม่ (Chrome 90+, Firefox 90+)
- Internet connection สำหรับ Deriv API
- GPU รองรับ WebGL (ถ้าต้องการใช้ GPU mode)

## หมายเหตุ
- ใช้ Deriv Demo App ID (1089) - ฟรี ไม่ต้องสมัคร
- ข้อมูลเป็น demo data จาก Deriv
- สามารถนำ Class ไปใช้ในโปรเจคอื่นได้ทันที
********************************************************************

# My Trading Library

Library รวม JavaScript สำหรับการเทรด, การวิเคราะห์ Technical Analysis, SMC (Smart Money Concepts), และ WebGPU Acceleration

## 📂 โครงสร้างไฟล์
ไฟล์ทั้งหมดอยู่ใน root directory เพื่อให้เรียกใช้ง่าย:
- `deriv-api.js`: API สำหรับเชื่อมต่อ Deriv
- `multi-asset-loader.js`: สำหรับดึงข้อมูลหลายคู่เงินพร้อมกัน
- `webgpu-indicators.js`: คำนวณอินดิเคเตอร์ด้วยการ์ดจอ (WebGPU)
- `indicators.js`: สูตรคำนวณพื้นฐาน (SMA, EMA, RSI, etc.)
- `SMCIndicator.js`: คำนวณ Smart Money Concepts
- `clsAnalysisGeneratorV2.js`: ตัวสร้างการวิเคราะห์รวม (SMC + Basic Indicators)

## 🚀 วิธีใช้งานผ่าน CDN (jsDelivr)

คุณสามารถเรียกไฟล์เหล่านี้ไปใช้ในโปรเจกต์อื่นได้ทันทีผ่าน CDN (โดยเปลี่ยน `[YourGitHubUsername]/[RepoName]` เป็นของคุณ):

```html
<!-- 1. Deriv API -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/deriv-api.js"></script>

<!-- 2. Basic Indicators -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/indicators.js"></script>

<!-- 3. SMC Indicator -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/SMCIndicator.standalone.js"></script>

<!-- 4. WebGPU (Optional) -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/webgpu-indicators.js"></script>

<!-- 5. Asset Loader -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/multi-asset-loader.js"></script>

<!-- 6. Analysis Generator -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/clsAnalysisGeneratorV2.js"></script>
```

อ่านรายละเอียดเพิ่มเติมได้ใน [SMC_Integration_Guide.md](SMC_Integration_Guide.md)

- 
