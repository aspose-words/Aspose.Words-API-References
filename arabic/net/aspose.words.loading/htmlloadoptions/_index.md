---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Loading.HtmlLoadOptions لتحسين تحميل مستند HTML في كائن مستند باستخدام خيارات قابلة للتخصيص للحصول على الأداء الأمثل.
type: docs
weight: 4070
url: /ar/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

يسمح بتحديد خيارات إضافية عند تحميل مستند HTML في[`Document`](../../aspose.words/document/) الكائن.

لمعرفة المزيد، قم بزيارة[تحديد خيارات التحميل](https://docs.aspose.com/words/net/specify-load-options/) مقالة توثيقية.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | يقوم بتهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | اختصار لتهيئة مثيل جديد لهذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | اختصار لتهيئة مثيل جديد لهذه الفئة مع تعيين الخصائص إلى القيم المحددة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | يحصل على السلسلة التي سيتم استخدامها لتحويل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة إليها أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | يحصل على قيمة تحدد كيفية استيراد خصائص عناصر مستوى الكتلة أو يعينها. القيمة الافتراضية هيMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل الملف التعريفي (Wmf أوEmf ) الصور إلىPngتنسيق الصورة. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. القيمة الافتراضية هي`خطأ شنيع` وإذا كان ذلك ممكنًا، يتم تخزين صور SVG المحملة كما هي دون تحويل. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | يحصل على أو يعين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون`باطل` . الافتراضي هو`باطل` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | يسمح بتحديد إعدادات خط المستند. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم تجاهل عناصر HTML &lt;noscript&gt;. القيمة الافتراضية هي`خطأ شنيع` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | يحدد ما إذا كان سيتم تجاهل بيانات OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | يحصل على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هيWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | يحصل على كلمة المرور لفتح مستند مشفر أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | يحصل على أو يعين النوع المفضل من عقد المستندات التي ستمثل عناصر &lt;input&gt; و&lt;select&gt; المستوردة. القيمة الافتراضية هيFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | يحصل على أو يعين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء تحميل مستند وتقبل البيانات حول تقدم التحميل. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عند استيراد مستند من HTML، MHTML. |
| [SupportFontFaceRules](../../aspose.words.loading/htmlloadoptions/supportfontfacerules/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم دعم قواعد @font-face وما إذا كان سيتم تحميل الخطوط المعلنة. القيمة الافتراضية هي`خطأ شنيع` . |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | يحصل على قيمة تشير إلى ما إذا كان سيتم دعم صور VML أم لا أو تعيينها. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | يسمح باستخدام الملفات المؤقتة عند قراءة المستند. بشكل افتراضي، هذه الخاصية هي`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | يحدد ما إذا كان سيتم تحديث الحقول باستخدام`متسخ` السمة. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم استخدام قيمة LCID التي تم الحصول عليها من سجل Windows لتحديد هوامش إعداد الصفحة الافتراضية. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | يتم استدعاؤها أثناء عملية التحميل، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | عدد الملي ثانية التي يجب انتظارها قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي ١٠٠٠٠٠ ميلي ثانية (١٠٠ ثانية). |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |

## أمثلة

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// إذا كانت القيمة صحيحة، فإننا نأخذ كود VML في الاعتبار أثناء تحليل المستند المحمّل.
loadOptions.SupportVml = supportVml;

// تحتوي هذه الوثيقة على صورة JPEG ضمن علامات "<!--[if gte vml 1]>"،
// وصورة PNG مختلفة ضمن علامات "<![if !vml]>".
// إذا قمنا بتعيين علامة "SupportVml" إلى "true"، فسوف يقوم Aspose.Words بتحميل ملف JPEG.
// إذا قمنا بتعيين هذا العلم إلى "false"، فسوف يقوم Aspose.Words بتحميل PNG فقط.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### أنظر أيضا

* class [LoadOptions](../loadoptions/)
* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
