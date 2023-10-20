---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldDatabase فصل. ينفذ حقل قاعدة البيانات في C#.
type: docs
weight: 1740
url: /ar/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

ينفذ حقل قاعدة البيانات.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldDatabase : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | الحصول على اتصال بالبيانات أو تعيينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | الحصول على أو تعيين المسار الكامل واسم الملف لقاعدة البيانات |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | الحصول على رقم السجل المتكامل لسجل البيانات الأول المراد إدراجه أو تعيينه. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | الحصول على أو تعيين سمات التنسيق التي سيتم تطبيقها على الجدول. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج أسماء الحقول من قاعدة البيانات كعناوين أعمدة في الجدول الناتج. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج البيانات في بداية عملية الدمج. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | الحصول على رقم السجل المتكامل لآخر سجل بيانات سيتم إدراجه أو تعيينه. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | الحصول على أو تعيين مجموعة من تعليمات SQL التي تستعلم عن قاعدة البيانات. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | الحصول على أو تعيين التنسيق الذي سيتم تطبيقه على نتيجة استعلام قاعدة البيانات. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

إدراج نتائج استعلام قاعدة البيانات في جدول WordprocessingML.

## أمثلة

يوضح كيفية استخراج البيانات من قاعدة البيانات وإدراجها كحقل في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيقوم حقل قاعدة البيانات هذا بتشغيل استعلام في قاعدة بيانات، ويعرض النتيجة في جدول.
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

// هذه الخصائص لها نفس وظيفة جمل LIMIT وTOP.
// قم بتكوينها لعرض الصفوف من 1 إلى 10 فقط من نتيجة الاستعلام في جدول الحقل.
field.FirstRecord = "1";
field.LastRecord = "10";

// هذه الخاصية هي فهرس التنسيق الذي نريد استخدامه لجدولنا. توجد قائمة تنسيقات الجدول في قائمة "التنسيق التلقائي للجدول...".
// الذي يظهر عندما نقوم بإنشاء حقل قاعدة بيانات في Microsoft Word. يتوافق الفهرس رقم 10 مع تنسيق "ملون 3".
field.TableFormat = "10";

// الخاصية FormatAttribute عبارة عن تمثيل سلسلة لعدد صحيح يقوم بتخزين أعلام متعددة.
// يمكننا تطبيق التنسيق الذي تشير إليه خاصية TableFormat بشكل وطني عن طريق تعيين علامات مختلفة في هذه الخاصية.
// الرقم الذي نستخدمه هو مجموع مجموعة من القيم المقابلة لجوانب مختلفة من نمط الجدول.
// 63 يمثل 1 (الحدود) + 2 (التظليل) + 4 (الخط) + 8 (اللون) + 16 (الاحتواء التلقائي) + 32 (صفوف العناوين).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
