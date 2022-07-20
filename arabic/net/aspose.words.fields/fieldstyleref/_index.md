---
title: FieldStyleRef
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ حقل STYLEREF .
type: docs
weight: 2290
url: /ar/net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

تنفيذ حقل STYLEREF .

```csharp
public class FieldStyleRef : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldStyleRef](fieldstyleref)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها تمامًا كما تظهر في المستند. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج رقم فقرة الفقرة المشار إليها في السياق الكامل. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج رقم فقرة الفقرة المشار إليها في السياق النسبي. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج الموضع النسبي للفقرة المشار إليها. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم البحث من أسفل الصفحة الحالية ، بدلاً من البحث من أعلى. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename) { get; set; } | الحصول على أو تحديد اسم النمط الذي يتم تنسيق النص المطلوب البحث عنه . |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم منع الأحرف غير المحددة. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يتم استخدام STYLEREF للإشارة إلى جزء من النص داخل المستند الذي تم تنسيقه باستخدام النمط المحدد.

### أمثلة

يوضح كيفية استخدام حقول STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء قائمة باستخدام قالب قائمة Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// ستعرض هذه القائمة التي تم إنشاؤها "1.a)".
 // المسافة قبل القوس هي حرف غير محدد ، يمكننا منعه.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// أضف نصًا وقم بتطبيق أنماط الفقرة التي ستشير إليها حقول STYLEREF.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// ضع حقل STYLEREF في الرأس واعرض أول نص على غرار "قائمة فقرة" في المستند.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// ضع حقل STYLEREF في التذييل ، واجعله يعرض آخر نص.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// يمكننا أيضًا استخدام حقول STYLEREF للإشارة إلى أرقام قائمة القوائم.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
