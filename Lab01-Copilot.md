Lab: สร้าง Web API (.NET) ด้วย GitHub Copilot

ขั้นตอนการทำ Lab

ขั้นตอนที่ 1: สร้างโปรเจกต์ใหม่<br>
	1.	เปิด VS Code และสร้าง repo ใหม่ (หรือเปิดโฟลเดอร์เปล่า)<br>
	2.	สั่งให้ Copilot สร้าง Web API โปรเจกต์:<br>
```bash
dotnet new webapi -n WebApi
cd WebApi
```

ขั้นตอนที่ 2: สร้าง API Endpoint<br>
	1.	เปิด WeatherForecastController.cs หรือสร้าง controller ใหม่ชื่อ MathController.cs<br>
	2.	ใช้ Copilot เพื่อ generate endpoint:<br>
	•	/factorial/{n}<br>
	•	/fibonacci/{n}<br><br>

ตัวอย่าง Prompt:<br>
```prompt
สร้าง API ที่รับพารามิเตอร์ n และคืนค่าผลลัพธ์ของ factorial
```

ขั้นตอนที่ 3: สร้าง Unit Test ด้วย Copilot Chat (15 นาที)<br>
	1.	สร้าง Project สำหรับ test:<br>
```bash
dotnet new xunit -n WebApi.Tests
dotnet add WebApi.Tests reference WebApi
```
