---
title: MarkdownLoadOptions Class
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.MarkdownLoadOptions لتحسين تجربة تحميل مستندات Markdown. خصّص الخيارات لدمجها بسلاسة في مشاريعك.
type: docs
weight: 4120
url: /ar/net/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class

يسمح بتحديد خيارات إضافية عند التحميلMarkdown وثيقة في[`Document`](../../aspose.words/document/) الكائن.

```csharp
public class MarkdownLoadOptions : LoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [MarkdownLoadOptions](markdownloadoptions/)() | يقوم بتهيئة مثيل جديد لـ`MarkdownLoadOptions` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | يحصل على السلسلة التي سيتم استخدامها لتحويل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة إليها أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل الملف التعريفي (Wmf أوEmf ) الصور إلىPngتنسيق الصورة. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | يحصل على أو يعين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون`باطل` . الافتراضي هو`باطل` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | يسمح بتحديد إعدادات خط المستند. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | يحدد ما إذا كان سيتم تجاهل بيانات OLE. |
| [ImportUnderlineFormatting](../../aspose.words.loading/markdownloadoptions/importunderlineformatting/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى التعرف على تسلسل مكون من حرفين زائد "++" كتنسيق نص مسطر. القيمة الافتراضية هي`خطأ شنيع` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | يحصل على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هيWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | يحصل على كلمة المرور لفتح مستند مشفر أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [PreserveEmptyLines](../../aspose.words.loading/markdownloadoptions/preserveemptylines/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم الاحتفاظ بالأسطر الفارغة أثناء تحميلMarkdown document. القيمة الافتراضية هي`خطأ شنيع` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | يحصل على أو يعين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء تحميل مستند وتقبل البيانات حول تقدم التحميل. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عند استيراد مستند من HTML، MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | يسمح باستخدام الملفات المؤقتة عند قراءة المستند. بشكل افتراضي، هذه الخاصية هي`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | يحدد ما إذا كان سيتم تحديث الحقول باستخدام`متسخ` السمة. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم استخدام قيمة LCID التي تم الحصول عليها من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | يتم استدعاؤها أثناء عملية التحميل، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |

## أمثلة

يوضح كيفية الحفاظ على السطر الفارغ أثناء تحميل المستند.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### أنظر أيضا

* class [LoadOptions](../loadoptions/)
* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
