---
title: FieldCitation
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ حقل CITATION .
type: docs
weight: 1530
url: /ar/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

تنفيذ حقل CITATION .

```csharp
public class FieldCitation : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldCitation](fieldcitation)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag) { get; set; } | الحصول على أو تعيين قيمة تحسب ال **بطاقة شعار** قيمة عنصر لمصدر آخر ليتم تضمينها في الاقتباس. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid) { get; set; } | الحصول على أو تحديد معرّف اللغة المستخدم مع النمط الببليوغرافي المحدد لتنسيق citation في المستند. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber) { get; set; } | الحصول على رقم الصفحة المقترن بالاقتباس أو تعيينه. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix) { get; set; } | الحصول على بادئة مُلحقة مسبقًا بالاقتباس أو تعيينها. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag) { get; set; } | الحصول على أو تعيين قيمة تحسب ال **بطاقة شعار**قيمة العنصر للمصدر المراد إدراجها . |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix) { get; set; } | الحصول على أو تعيين لاحقة ملحقة بالاقتباس. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor) { get; set; } | الحصول على أو تحديد ما إذا كانت معلومات المؤلف ممنوعة من الاقتباس. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle) { get; set; } | الحصول على أو تحديد ما إذا كان قد تم منع معلومات العنوان من الاقتباس. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear) { get; set; } | الحصول على أو تحديد ما إذا كانت معلومات السنة محجوبة من الاقتباس. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber) { get; set; } | الحصول على أو تحديد رقم المجلد المرتبط بالاقتباس. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يتم إدراج محتويات ملف **مصدر** عنصر مع محدد **بطاقة شعار** عنصر باستخدام نمط ببليوغرافي .

### أمثلة

يوضح كيفية العمل مع حقلي CITATION و BIBLIOGRAPHY.

```csharp
// افتح مستندًا يحتوي على مصادر ببليوغرافية يمكننا العثور عليها
// Microsoft Word عبر المراجع - >; الاقتباسات وأمبير. ببليوغرافيا - >. إدارة المصادر.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// أنشئ اقتباسًا برقم الصفحة فقط ومؤلف الكتاب المشار إليه.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// نشير إلى المصادر باستخدام أسماء العلامات الخاصة بهم.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// إنشاء اقتباس أكثر تفصيلاً يستشهد بمصدرين.
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

// يمكننا استخدام حقل ببليوجرافي لعرض جميع المصادر داخل المستند.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
