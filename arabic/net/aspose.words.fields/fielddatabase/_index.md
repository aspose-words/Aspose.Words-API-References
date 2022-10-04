---
title: FieldDatabase
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ حقل قاعدة البيانات .
type: docs
weight: 1590
url: /ar/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

تنفيذ حقل قاعدة البيانات .

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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | الحصول على أو تحديد المسار الكامل واسم الملف لقاعدة البيانات |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | الحصول على أو تعيين رقم السجل المتكامل لسجل البيانات الأول المراد إدراجه . |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | الحصول على أو تحديد سمات التنسيق التي سيتم تطبيقها على الجدول. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج أسماء الحقول من قاعدة البيانات كعناوين أعمدة في الجدول الناتج. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج البيانات في بداية الدمج. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | الحصول على أو تعيين رقم السجل المتكامل لآخر سجل بيانات لإدراجه . |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | الحصول على أو تعيين مجموعة من تعليمات SQL التي تستعلم عن قاعدة البيانات. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | الحصول على أو تحديد التنسيق الذي سيتم تطبيقه على نتيجة استعلام قاعدة البيانات. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove/)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

إدراج نتائج استعلام قاعدة البيانات في جدول معالجة Word.

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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
