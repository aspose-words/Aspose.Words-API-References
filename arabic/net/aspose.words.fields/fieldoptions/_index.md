---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldOptions لتحسين التعامل مع الحقول في المستندات، مما يعزز سير عملك وكفاءة إدارة المستندات.
type: docs
weight: 2660
url: /ar/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

يمثل خيارات للتحكم في التعامل مع الحقول في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public sealed class FieldOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | يحصل على مولد الباركود المخصص أو يعينه. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | يحصل على أو يعين موفرًا يعيد نمط ببليوغرافيا لـ [`FieldBibliography`](../fieldbibliography/) و[`FieldCitation`](../fieldcitation/) الحقول. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | يحصل على مسارات قوالب MS Word المضمنة أو يعينها. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | يحصل على أو يعين مُقيِّم تعبيرات مقارنة الحقل. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | يحصل على معلومات المستخدم الحالية أو يعينها. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | يحصل على أو يعين فاصل النمط المخصص لمفتاح \t في[`FieldToc`](../fieldtoc/) الحقل. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | يحصل على اسم مؤلف المستند الافتراضي أو يعيّنه. إذا كان اسم المؤلف محددًا مسبقًا في خصائص المستند المضمنة، فلن يُؤخذ هذا الخيار في الاعتبار. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | يحصل على أو يعين موفرًا يعيد نتيجة استعلام لـ[`FieldDatabase`](../fielddatabase/) الحقل. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | يحصل على أو يعين[`FieldIndexFormat`](./fieldindexformat/) الذي يمثل التنسيق لـ[`FieldIndex`](../fieldindex/) الحقول في المستند. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | يحصل على أو يعين موفرًا يعيد كائن ثقافة محددًا لكل حقل معين. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | يحدد الثقافة التي سيتم استخدامها لتنسيق نتيجة الحقل. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | يحصل أو يعين[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) التنفيذ |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | يحصل أو يعين[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) التنفيذ. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | يحصل على اسم ملف المستند أو يعينه. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | يحصل على القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا أو يعينها. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | يحصل على القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم (الأقدم من AW 13.10) للحقول ممكّنًا أم لا أو يعينها. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | يحصل على الثقافة أو يعينها لمعالجة قيم الحقول مسبقًا. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | يسمح بالتحكم في كيفية تنسيق نتيجة الحقل. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | يحصل على اسم ملف القالب الذي يستخدمه المستند أو يعينه. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | يحصل على فئات جدول السلطات أو يعينها. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | يحصل على القيمة أو يعينها للإشارة إلى أن تنسيق الرقم يتم تحليله باستخدام ثقافة ثابتة أم لا |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | يحصل على المستجيب أو يعينه على مطالبات المستخدم أثناء تحديث الحقل. |

## أمثلة

يوضح كيفية تحديد مصدر الثقافة المستخدمة لتنسيق التاريخ أثناء تحديث الحقل أو دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلي دمج باللغة الألمانية.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// قم بتعيين الثقافة الحالية إلى اللغة الإنجليزية الأمريكية بعد الحفاظ على قيمتها الأصلية في المتغير.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// سيستخدم هذا الدمج ثقافة الموضوع الحالي لتنسيق التاريخ، باللغة الإنجليزية الأمريكية.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// قم بتكوين الدمج التالي للحصول على قيمة ثقافته من رمز الحقل. ستكون قيمة هذه الثقافة بالألمانية.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// تحتوي نتيجة الدمج الأولى على تاريخ بتنسيق اللغة الإنجليزية، بينما النتيجة الثانية باللغة الألمانية.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

//استعادة ثقافة الموضوع الأصلية.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
