---
title: FieldOptions
second_title: Aspose.Words لمراجع .NET API
description: يمثل خيارات للتحكم في معالجة الحقول في المستند.
type: docs
weight: 2100
url: /ar/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

يمثل خيارات للتحكم في معالجة الحقول في المستند.

```csharp
public sealed class FieldOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | الحصول على أو تعيين مولد الباركود المخصص. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | الحصول على أو تعيين مسارات قوالب MS Word المضمنة. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | الحصول على أو تعيين مقيِّم تعبيرات مقارنة الحقول. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | الحصول على أو تعيين معلومات المستخدم الحالية. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | الحصول على أو تعيين فاصل نمط مخصص للمحول \ t[`FieldToc`](../fieldtoc/) الحقل . |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | الحصول على أو تعيين اسم مؤلف المستند الافتراضي. إذا كان اسم المؤلف محددًا بالفعل في خصائص المستند المضمنة ، فلن يتم اعتبار هذا الخيار . |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | الحصول على أو تعيين موفر يقوم بإرجاع نتيجة استعلام لـ[`FieldDatabase`](../fielddatabase/) الحقل . |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | يحصل أو يحدد أ[`FieldIndexFormat`](./fieldindexformat/) الذي يمثل تنسيق ملف[`FieldIndex`](../fieldindex/)الحقول في المستند. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | الحصول على أو تعيين موفر يقوم بإرجاع كائن ثقافة محدد لكل حقل معين. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | تحدد الثقافة المراد استخدامها لتنسيق نتيجة الحقل. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | يحصل أو يحدد[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) تنفيذ |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | الحصول على أو تحديد اسم ملف المستند. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | الحصول على القيمة أو تعيينها للإشارة إلى ما إذا كان تنسيق الأرقام القديم (أقدم من AW 13.10) للحقول ممكّنًا أم لا. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | الحصول على الثقافة أو تعيينها لقيم حقل المعالجة المسبقة. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | يسمح بالتحكم في كيفية تنسيق نتيجة الحقل. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | الحصول على أو تحديد اسم ملف النموذج المستخدم في المستند. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | الحصول على أو تعيين جدول فئات المصادر . |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | الحصول على أو تعيين القيمة التي تشير إلى أن تنسيق الأرقام يتم تحليله باستخدام ثقافة ثابتة أو لا |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | الحصول على أو تعيين المستجيب لمطالبات المستخدم أثناء تحديث الحقل. |

### أمثلة

يوضح كيفية تحديد مصدر الثقافة المستخدمة لتنسيق التاريخ أثناء تحديث الحقل أو دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلي دمج باستخدام اللغة الألمانية.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// اضبط الثقافة الحالية على اللغة الإنجليزية الأمريكية بعد الاحتفاظ بقيمتها الأصلية في متغير.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// سيستخدم هذا الدمج ثقافة مؤشر الترابط الحالي لتنسيق التاريخ ، باللغة الإنجليزية الأمريكية.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// تكوين الدمج التالي للحصول على قيمة ثقافته من رمز الحقل. قيمة هذه الثقافة ستكون ألمانية.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// تحتوي نتيجة الدمج الأولى على تاريخ تم تنسيقه باللغة الإنجليزية ، بينما تحتوي النتيجة الثانية على تاريخ باللغة الألمانية.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// استعادة الثقافة الأصلية للخيط.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
