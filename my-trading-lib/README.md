# My Trading Library

Library รวม JavaScript สำหรับการเทรด, การวิเคราะห์ Technical Analysis, SMC (Smart Money Concepts), และ WebGPU Acceleration

## 📂 โครงสร้างไฟล์
- `deriv-api.js`: API สำหรับเชื่อมต่อ Deriv
- `multi-asset-loader.js`: สำหรับดึงข้อมูลหลายคู่เงินพร้อมกัน
- `webgpu-indicators.js`: คำนวณอินดิเคเตอร์ด้วยการ์ดจอ (WebGPU)
- `js/indicators.js`: สูตรคำนวณพื้นฐาน (SMA, EMA, RSI, etc.)
- `js/SMCIndicator.js`: คำนวณ Smart Money Concepts
- `js/clsAnalysisGeneratorV2.js`: ตัวสร้างการวิเคราะห์รวม (SMC + Basic Indicators)

## 🚀 วิธีใช้งานผ่าน CDN (jsDelivr)

คุณสามารถเรียกไฟล์เหล่านี้ไปใช้ในโปรเจกต์อื่นได้ทันทีผ่าน CDN:

```html
<!-- 1. Deriv API -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/deriv-api.js"></script>

<!-- 2. Basic Indicators -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/js/indicators.js"></script>

<!-- 3. SMC Indicator -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/js/SMCIndicator.standalone.js"></script>

<!-- 4. WebGPU (Optional) -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/webgpu-indicators.js"></script>

<!-- 5. Asset Loader -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/multi-asset-loader.js"></script>

<!-- 6. Analysis Generator -->
<script src="https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[RepoName]@main/js/clsAnalysisGeneratorV2.js"></script>
```

อ่านรายละเอียดเพิ่มเติมได้ใน [SMC_Integration_Guide.md](SMC_Integration_Guide.md)
