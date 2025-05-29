---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.TxtLoadOptions لتحسين تحميل مستندات النصوص. خصّص مستندك بخيارات مرنة لتحقيق أداء مثالي.
type: docs
weight: 4190
url: /ar/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

يسمح بتحديد خيارات إضافية عند التحميلText وثيقة في[`Document`](../../aspose.words/document/) الكائن.

لمعرفة المزيد، قم بزيارة[تحديد خيارات التحميل](https://docs.aspose.com/words/net/specify-load-options/) مقالة توثيقية.

```csharp
public class TxtLoadOptions : LoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | يقوم بتهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى أن الكشف التلقائي عن الترقيم سيتم إجراؤه أثناء تحميل مستند. القيمة الافتراضية هي`حقيقي` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | يحصل على السلسلة التي سيتم استخدامها لتحويل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة إليها أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل الملف التعريفي (Wmf أوEmf ) الصور إلىPngتنسيق الصورة. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math. |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } | يحدد إما اكتشاف الارتباطات التشعبية في النص. القيمة الافتراضية هي`خطأ شنيع` . |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | يسمح بتحديد كيفية التعرف على عناصر القائمة المرقمة عند استيراد المستند من تنسيق نص عادي. القيمة الافتراضية هي`حقيقي`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | يحصل على اتجاه المستند أو يعينه. القيمة الافتراضية هيLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | يحصل على أو يعين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون`باطل` . الافتراضي هو`باطل` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | يسمح بتحديد إعدادات خط المستند. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | يحدد ما إذا كان سيتم تجاهل بيانات OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | يحصل على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | يحصل على الخيار المفضل للتعامل مع المسافة البادئة أو يعينه. القيمة الافتراضية هيConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هيWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | يحصل على كلمة المرور لفتح مستند مشفر أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | يحصل على أو يعين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء تحميل مستند وتقبل البيانات حول تقدم التحميل. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عند استيراد مستند من HTML، MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | يسمح باستخدام الملفات المؤقتة عند قراءة المستند. بشكل افتراضي، هذه الخاصية هي`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | يحصل على الخيار المفضل لمعالجة المسافة الزائدة أو يعينه. القيمة الافتراضية هيTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | يحدد ما إذا كان سيتم تحديث الحقول باستخدام`متسخ` السمة. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم استخدام قيمة LCID التي تم الحصول عليها من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | يتم استدعاؤها أثناء عملية التحميل، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |

## أمثلة

يوضح كيفية قراءة الروابط التشعبية وعرضها.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // تحميل المستند بالارتباطات التشعبية.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    //طباعة نص الارتباطات التشعبية.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### أنظر أيضا

* class [LoadOptions](../loadoptions/)
* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
