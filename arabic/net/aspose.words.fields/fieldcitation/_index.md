---
title: Class FieldCitation
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldCitation فصل. ينفذ حقل CITATION.
type: docs
weight: 1680
url: /ar/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

ينفذ حقل CITATION.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldCitation : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldCitation](fieldcitation/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag/) { get; set; } | الحصول على أو تعيين قيمة تطابق **بطاقة شعار** قيمة العنصر لمصدر آخر ليتم تضمينه في الاقتباس. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid/) { get; set; } | الحصول على أو تعيين معرف اللغة المستخدم مع النمط الببليوغرافي المحدد لتنسيق الاقتباس في المستند. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber/) { get; set; } | الحصول على أو تعيين رقم الصفحة المرتبطة بالاقتباس. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix/) { get; set; } | الحصول على أو تعيين بادئة مُلحقة بالاقتباس. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag/) { get; set; } | الحصول على أو تعيين قيمة تطابق **بطاقة شعار** قيمة العنصر للمصدر المراد إدراجه. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix/) { get; set; } | الحصول على أو تعيين اللاحقة الملحقة بالاقتباس. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم حذف معلومات المؤلف من الاقتباس. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم حذف معلومات العنوان من الاقتباس. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم حذف معلومات السنة من الاقتباس. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber/) { get; set; } | الحصول على أو تعيين رقم المجلد المرتبط بالاستشهاد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يقوم بإدراج محتويات الملف **مصدر** عنصر مع المحدد **بطاقة شعار** عنصر باستخدام النمط الببليوغرافي.

### أمثلة

يوضح كيفية العمل مع حقول CITATION وBIBLIOGRAPHY.

```csharp
// افتح مستندًا يحتوي على مصادر ببليوغرافية يمكننا العثور عليها
// Microsoft Word عبر المراجع -> اقتباسات & قائمة المراجع -> إدارة المصادر.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// أنشئ اقتباسًا باستخدام رقم الصفحة ومؤلف الكتاب المشار إليه فقط.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// نشير إلى المصادر باستخدام أسماء علاماتها.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// قم بإنشاء اقتباس أكثر تفصيلاً يستشهد بمصدرين.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// يمكننا استخدام حقل الببليوغرافيا لعرض كافة المصادر داخل الوثيقة.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


