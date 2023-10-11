---
title: Class FieldOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldOptions فصل. يمثل خيارات للتحكم في المعالجة الميدانية في المستند.
type: docs
weight: 2250
url: /ar/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

يمثل خيارات للتحكم في المعالجة الميدانية في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public sealed class FieldOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | الحصول على أو تعيين مولد باركود مخصص. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | الحصول على أو تعيين موفر يُرجع نمط المراجع لـ [`FieldBibliography`](../fieldbibliography/) و[`FieldCitation`](../fieldcitation/) الحقول. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | الحصول على أو تعيين مسارات قوالب MS Word المضمنة. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | الحصول على أو تعيين مقيم تعبيرات مقارنة الحقول. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | الحصول على معلومات المستخدم الحالية أو تعيينها. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | الحصول على فاصل نمط مخصص أو تعيينه للتبديل \t[`FieldToc`](../fieldtoc/) الحقل. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | الحصول على أو تعيين اسم مؤلف المستند الافتراضي. إذا كان اسم المؤلف محددًا بالفعل في خصائص المستند المضمنة، فلن يتم أخذ هذا الخيار في الاعتبار. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | الحصول على أو تعيين موفر يقوم بإرجاع نتيجة استعلام لـ[`FieldDatabase`](../fielddatabase/) الحقل. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | الحصول على أو تعيين a[`FieldIndexFormat`](./fieldindexformat/) الذي يمثل التنسيق لـ[`FieldIndex`](../fieldindex/) الحقول في الوثيقة. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | الحصول على أو تعيين الموفر الذي يُرجع كائن الثقافة الخاص بكل حقل معين. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | يحدد الثقافة التي سيتم استخدامها لتنسيق نتيجة الحقل. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | يحصل على أو مجموعات[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) التنفيذ |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | يحصل على أو مجموعات[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) التنفيذ. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | الحصول على اسم ملف المستند أو تعيينه. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء التحديث الميداني أم لا. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | الحصول على القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم (أقدم من AW 13.10) للحقول أو تعيينه ممكنًا أم لا. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | الحصول على الثقافة أو تعيينها لمعالجة قيم الحقول مسبقًا. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | يسمح بالتحكم في كيفية تنسيق نتيجة الحقل. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | الحصول على أو تعيين اسم ملف القالب الذي يستخدمه المستند. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | الحصول على أو تعيين جدول فئات المراجع. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | الحصول على أو تعيين القيمة التي تشير إلى أنه تم تحليل تنسيق الأرقام باستخدام الثقافة الثابتة أو not |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | الحصول على المستجيب أو تعيينه لمطالبات المستخدم أثناء التحديث الميداني. |

### أمثلة

يوضح كيفية تحديد مصدر الثقافة المستخدمة لتنسيق التاريخ أثناء تحديث الحقل أو دمج المراسلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلين مدمجين باللغة الألمانية.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// اضبط الثقافة الحالية على اللغة الإنجليزية الأمريكية بعد الحفاظ على قيمتها الأصلية في متغير.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// سيستخدم هذا الدمج ثقافة الموضوع الحالي لتنسيق التاريخ، باللغة الإنجليزية الأمريكية.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// قم بتكوين الدمج التالي لمصدر قيمة الثقافة الخاصة به من رمز الحقل. وستكون قيمة تلك الثقافة ألمانية.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// تحتوي نتيجة الدمج الأولى على تاريخ منسق باللغة الإنجليزية، بينما تحتوي النتيجة الثانية على تاريخ منسق باللغة الألمانية.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// استعادة الثقافة الأصلية للخيط.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


