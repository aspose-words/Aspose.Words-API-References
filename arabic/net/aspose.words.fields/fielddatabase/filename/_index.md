---
title: FieldDatabase.FileName
second_title: Aspose.Words لمراجع .NET API
description: FieldDatabase ملكية. الحصول على أو تحديد المسار الكامل واسم الملف لقاعدة البيانات
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fielddatabase/filename/
---
## FieldDatabase.FileName property

الحصول على أو تحديد المسار الكامل واسم الملف لقاعدة البيانات

```csharp
public string FileName { get; set; }
```

### أمثلة

يوضح كيفية استخراج البيانات من قاعدة بيانات وإدراجها كحقل في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيجري حقل قاعدة البيانات هذا استعلامًا في قاعدة بيانات ، ويعرض النتيجة في جدول.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d \"{DatabaseDir.Replace("\\", "\\\\") + "Northwind.mdb"}\" \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", 
    field.GetFieldCode());

// أدخل حقل قاعدة بيانات آخر باستخدام استعلام أكثر تعقيدًا يقوم بفرز جميع المنتجات بترتيب تنازلي حسب إجمالي المبيعات.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// هذه الخصائص لها نفس وظيفة جمل LIMIT و TOP.
// قم بتكوينها لعرض الصفوف من 1 إلى 10 فقط من نتيجة الاستعلام في جدول الحقل.
field.FirstRecord = "1";
field.LastRecord = "10";

// هذه الخاصية هي فهرس التنسيق الذي نريد استخدامه لجدولنا. قائمة تنسيقات الجدول موجودة في قائمة "تنسيق تلقائي للجدول ..."
// الذي يظهر عندما نقوم بإنشاء حقل قاعدة بيانات في Microsoft Word. الفهرس رقم 10 يتوافق مع تنسيق "ملون 3".
field.TableFormat = "10";

// خاصية FormatAttribute هي تمثيل سلسلة لعدد صحيح يخزن أعلام متعددة.
// يمكننا تطبيق التنسيق الأبوي الذي تشير إليه خاصية TableFormat عن طريق تعيين علامات مختلفة في هذه الخاصية.
// الرقم الذي نستخدمه هو مجموع مجموعة القيم المقابلة لجوانب مختلفة من نمط الجدول.
// 63 يمثل 1 (حدود) + 2 (تظليل) + 4 (خط) + 8 (لون) + 16 (احتواء تلقائي) + 32 (صفوف عناوين).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### أنظر أيضا

* class [FieldDatabase](../)
* مساحة الاسم [Aspose.Words.Fields](../../fielddatabase/)
* المجسم [Aspose.Words](../../../)


