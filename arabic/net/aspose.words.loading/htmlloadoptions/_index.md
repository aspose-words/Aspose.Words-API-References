---
title: HtmlLoadOptions
second_title: Aspose.Words لمراجع .NET API
description: يسمح بتحديد خيارات إضافية عند تحميل مستند HTML في ملفDocument../aspose.words/document/ الكائن .
type: docs
weight: 3420
url: /ar/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

يسمح بتحديد خيارات إضافية عند تحميل مستند HTML في ملف[`Document`](../../aspose.words/document/) الكائن .

```csharp
public class HtmlLoadOptions : LoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | اختصار لتهيئة مثيل جديد من هذه الفئة بكلمة المرور المحددة لتحميل مستند مشفر. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | اختصار لتهيئة مثيل جديد من هذه الفئة بخصائص معينة للقيم المحددة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | الحصول على أو تعيين السلسلة التي سيتم استخدامها لحل URIs النسبية الموجودة في المستند إلى URIs المطلقة عند الحاجة . يمكن أن تكون سلسلة فارغة أو فارغة. الافتراضي هو فارغ. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية استيراد خصائص عناصر مستوى الكتلة. القيمة الافتراضية هيMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تحويل ملف تعريف (Wmf أوEmf ) صور لPng تنسيق الصورة . |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تحويل الأشكال باستخدام EquationXML إلى كائنات Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. القيمة الافتراضية هي`خاطئة` وإذا أمكن ، يتم تخزين صور SVG المحملة كما هي بدون تحويل. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | الحصول على أو تعيين الترميز الذي سيتم استخدامه لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون فارغًا. الافتراضي هو فارغ. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | يسمح بتحديد إعدادات خط الوثيقة. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى تجاهل عناصر HTML &lt;noscript&gt; . القيمة الافتراضية هي`خاطئة` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | الحصول على تفضيلات اللغة التي سيتم استخدامها عند تحميل المستند. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | يحدد تنسيق المستند الذي سيتم تحميله. الافتراضي هوAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هيWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | الحصول على كلمة المرور أو تعيينها لفتح مستند مشفر. يمكن أن تكون سلسلة فارغة أو فارغة. الافتراضي هو فارغ. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | الحصول على أو تعيين النوع المفضل لعقد المستندات التي ستمثل العناصر المستوردة &lt;input&gt; و &lt;select&gt; . القيمة الافتراضية هيFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word . القيمة الافتراضية هي false . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء تحميل مستند ويقبل البيانات حول تقدم التحميل. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور ، أوراق الأنماط) عند استيراد مستند من HTML ، MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم دعم صور VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | يسمح باستخدام الملفات المؤقتة عند قراءة المستند. افتراضيًا ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | يحدد ما إذا كان سيتم تحديث الحقول بامتداد`متسخ` السمة . |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | تم الاستدعاء أثناء عملية التحميل ، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | عدد المللي ثانية المطلوب انتظاره قبل انتهاء مهلة طلب الويب. القيمة الافتراضية هي 100000 مللي ثانية (100 ثانية) . |

### أنظر أيضا

* class [LoadOptions](../loadoptions/)
* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
