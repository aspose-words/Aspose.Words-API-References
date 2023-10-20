---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Loading.HtmlLoadOptions فصل. يسمح بتحديد خيارات إضافية عند تحميل مستند HTML في ملفDocument الكائن في C#.
type: docs
weight: 3620
url: /ar/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

يسمح بتحديد خيارات إضافية عند تحميل مستند HTML في ملف[`Document`](../../aspose.words/document/) الكائن.

لمعرفة المزيد، قم بزيارة[تحديد خيارات التحميل](https://docs.aspose.com/words/net/specify-load-options/) مقالة توثيقية.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | اختصار لتهيئة مثيل جديد لهذه الفئة بكلمة المرور المحددة لتحميل مستند مشفر. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | اختصار لتهيئة مثيل جديد لهذه الفئة مع تعيين الخصائص على القيم المحددة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | الحصول على أو تعيين السلسلة التي سيتم استخدامها لتحليل معرفات URI النسبية الموجودة في المستند إلى معرفات URI مطلقة عند الحاجة. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية استيراد خصائص عناصر مستوى الكتلة. القيمة الافتراضية هيMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل ملف التعريف (Wmf أوEmf ) الصور لPng تنسيق الصورة. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. القيمة الافتراضية هي`خطأ شنيع` وإذا أمكن، يتم تخزين صور SVG المحملة كما هي بدون تحويل. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | الحصول على أو تعيين التشفير الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد التشفير داخل المستند. يمكن أن يكون`باطل` . الافتراضي هو`باطل` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | يسمح بتحديد إعدادات خط المستند. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم تجاهل عناصر HTML &lt;noscript&gt; أم لا. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | يحدد ما إذا كان سيتم تجاهل بيانات OLE أم لا. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | يحصل على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار معين من MS Word. القيمة الافتراضية هيWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | الحصول على كلمة المرور أو تعيينها لفتح مستند مشفر. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | الحصول على أو تعيين النوع المفضل لعقد المستند التي ستمثل عناصر &lt;input&gt; و&lt;select&gt; المستوردة. القيمة الافتراضية هيFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء تحميل مستند ويقبل البيانات المتعلقة بتقدم التحميل. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عند استيراد مستند من HTML، MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم دعم صور VML أم لا. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | يسمح باستخدام الملفات المؤقتة عند قراءة المستند. بشكل افتراضي هذه الخاصية هي`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | يحدد ما إذا كان سيتم تحديث الحقول ذات الامتداد أم لا`متسخ` السمة. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | يتم استدعاؤه أثناء عملية التحميل، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | عدد المللي ثانية التي يجب انتظارها قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية (100 ثانية). |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) |  |

### أنظر أيضا

* class [LoadOptions](../loadoptions/)
* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
