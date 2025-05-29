---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldDatabase لتطبيق حقول قاعدة البيانات بكفاءة في مستنداتك. حسّن أتمتة مستنداتك اليوم!
type: docs
weight: 2150
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
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | يحصل على اتصال بالبيانات أو يعينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | يحصل على المسار الكامل واسم الملف لقاعدة البيانات أو يعينه |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | يحصل على رقم السجل الصحيح لسجل البيانات الأول الذي سيتم إدراجه أو يعينه. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | يحصل على أو يعين السمات التي سيتم تطبيقها على الجدول. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إدراج أسماء الحقول من قاعدة البيانات كعناوين أعمدة في الجدول الناتج. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إدراج البيانات في بداية الدمج. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | يحصل على رقم السجل الصحيح لسجل البيانات الأخير المراد إدراجه أو يعينه. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | يحصل على مجموعة من تعليمات SQL التي تستفسر عن قاعدة البيانات أو يعينها. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | يحصل على التنسيق الذي سيتم تطبيقه على نتيجة استعلام قاعدة البيانات أو يعينه. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

يقوم بإدراج نتائج استعلام قاعدة البيانات في جدول WordprocessingML.

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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
