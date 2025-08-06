Lab: สร้าง Web API (.NET) ด้วย GitHub Copilot

ขั้นตอนการทำ Lab<br>

ขั้นตอนที่ 1: สร้างโปรเจกต์ใหม่<br>
	1.	เปิด VS Code และสร้าง repo ใหม่ (หรือเปิดโฟลเดอร์เปล่า)<br>
	2.	สั่งให้ Copilot สร้าง Web API โปรเจกต์:<br>
```bash
dotnet new webapi -n WebApi
cd WebApi
```

ขั้นตอนที่ 2: สร้าง Model และ Repository <br>
•	ใช้ Prompt ให้ Copilot สร้างคลาส Product.cs:<br>
```prompt
สร้างคลาส Product ที่มี Id, Name, Price, และ Stock
```
•	สร้าง IProductRepository แบบ In-Memory:<br>
```prompt
สร้าง interface สำหรับ CRUD ของ Product และ class ที่ implement แบบ in-memory
```

ขั้นตอนที่ 3: สร้าง Controller พร้อม CRUD <br>
•	สร้าง ProductController.cs:<br>
```prompt
สร้าง Web API controller สำหรับ Product ที่มี action: GetAll, GetById, Create, Update, Delete
```
•	ให้ Copilot แนะนำ route และ action method:<br>
```csharp
[HttpGet]
public IEnumerable<Product> GetAll()

[HttpGet("{id}")]
public ActionResult<Product> GetById(int id)

[HttpPost]
public IActionResult Create(Product product)

[HttpPut("{id}")]
public IActionResult Update(int id, Product product)

[HttpDelete("{id}")]
public IActionResult Delete(int id)
```
