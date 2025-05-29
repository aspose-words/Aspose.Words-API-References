---
title: IFieldDatabaseProvider Interface
linktitle: IFieldDatabaseProvider
articleTitle: IFieldDatabaseProvider
second_title: Aspose.Words لـ .NET
description: حسّن أتمتة مستنداتك باستخدام واجهة Aspose.Words.Fields.IFieldDatabaseProvider. وفّر بيانات تحديثات FieldDatabase بسلاسة.
type: docs
weight: 3100
url: /ar/net/aspose.words.fields/ifielddatabaseprovider/
---
## IFieldDatabaseProvider interface

قم بتنفيذ هذه الواجهة لتوفير البيانات لـ[`FieldDatabase`](../fielddatabase/) الحقل عندما يتم تحديثه.

```csharp
public interface IFieldDatabaseProvider
```

## طُرق

| اسم | وصف |
| --- | --- |
| [GetQueryResult](../../aspose.words.fields/ifielddatabaseprovider/getqueryresult/)(*string, string, string, [FieldDatabase](../fielddatabase/)*) | إرجاع نتيجة الاستعلام. |

## أمثلة

يوضح كيفية استخراج البيانات من قاعدة البيانات وإدراجها كحقل في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيقوم حقل قاعدة البيانات هذا بتشغيل استعلام على قاعدة البيانات، وعرض النتيجة في جدول.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// قم بإدراج حقل قاعدة بيانات آخر باستخدام استعلام أكثر تعقيدًا يقوم بفرز جميع المنتجات بترتيب تنازلي حسب إجمالي المبيعات.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// هذه الخصائص لها نفس وظيفة جملتي LIMIT وTOP.
// قم بتكوينها لعرض الصفوف من 1 إلى 10 فقط من نتيجة الاستعلام في جدول الحقل.
field.FirstRecord = "1";
field.LastRecord = "10";

// هذه الخاصية هي فهرس التنسيق الذي نريد استخدامه لجدولنا. قائمة تنسيقات الجدول موجودة في قائمة "تنسيق الجدول تلقائيًا..."
// يظهر هذا عند إنشاء حقل قاعدة بيانات في مايكروسوفت وورد. الفهرس رقم ١٠ يتوافق مع تنسيق "Colorful 3".
field.TableFormat = "10";

// خاصية FormatAttribute عبارة عن تمثيل سلسلة لعدد صحيح يخزن أعلامًا متعددة.
// يمكننا تطبيق التنسيق الذي تشير إليه خاصية TableFormat بشكل أصيل عن طريق تعيين علامات مختلفة في هذه الخاصية.
// الرقم الذي نستخدمه هو مجموع مجموعة من القيم المقابلة لجوانب مختلفة من نمط الجدول.
// 63 يمثل 1 (الحدود) + 2 (التظليل) + 4 (الخط) + 8 (اللون) + 16 (التوافق التلقائي) + 32 (صفوف العناوين).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
