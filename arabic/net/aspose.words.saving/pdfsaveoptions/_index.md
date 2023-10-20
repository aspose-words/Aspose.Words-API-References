---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.PdfSaveOptions فصل. يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند في ملفPdf التنسيق في C#.
type: docs
weight: 5520
url: /ar/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند في ملفPdf التنسيق.

لمعرفة المزيد، قم بزيارة[حدد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | تهيئة مثيل جديد لهذه الفئة والذي يمكن استخدامه لحفظ مستند في Pdf التنسيق. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | علامة تحدد ما إذا كان سيتم كتابة عوامل إضافية لتحديد موضع النص أم لا. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم السماح بدمج الخطوط باستخدام مخططات PostScript عند حفظ تضمين خطوط TrueType في مستند. القيمة الافتراضية هي`خطأ شنيع` . |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم تخزين الرسومات الموضوعة في خلفية المستند أم لا. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | يحدد مستوى التوافق مع معايير PDF لمستندات المخرجات. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | يحدد ما إذا كان سيتم تحويل مراجع الحواشي السفلية/التعليقات الختامية في القصة النصية الرئيسية إلى ارتباطات تشعبية نشطة. عند النقر فوق الارتباط التشعبي سيؤدي إلى الحاشية السفلية/التعليقات الختامية المقابلة. الافتراضي هو`خطأ شنيع` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | الحصول على أو تحديد قيمة تحدد الطريق[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) يتم تصديرها إلى ملف PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | الحصول على أو تعيين المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | الحصول على أو تعيين تفاصيل التوقيع على مستند PDF الناتج. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | علامة تحدد ما إذا كان شريط عنوان النافذة يجب أن يعرض عنوان المستند المأخوذ من مدخل العنوان في قاموس معلومات المستند. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض التأثيرات ثلاثية الأبعاد. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض تأثيرات DrawML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawML. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | يسمح بتحديد خيارات الاختزال. |
| [EmbedAttachments](../../aspose.words.saving/pdfsaveoptions/embedattachments/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم تضمين المرفقات في مستند PDF أم لا. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | الحصول على أو تعيين تفاصيل تشفير مستند PDF الناتج. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان سيتم تصدير بنية المستند أم لا. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | متى`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم إنشاء علامة "Span" في بنية المستند لتصدير لغة النص أم لا. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب وضع علامة على رسم الفقرة كقطعة أثرية. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | يحدد وضع تضمين الخط. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | يحدد كيفية تصدير الإشارات المرجعية في الرؤوس/التذييلات. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | يحدد كيفية تحديد مساحة اللون للصور في مستند PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | يحدد نوع الضغط الذي سيتم استخدامه لجميع الصور في المستند. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض كائنات الحبر (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | علامة تشير إلى ما إذا كان سيتم تنفيذ استكمال الصورة بواسطة قارئ مطابق. متى`خطأ شنيع` تم تحديده، ولم تتم كتابة العلامة في مستند الإخراج و يتم استخدام السلوك الافتراضي للقارئ بدلاً من ذلك. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | الحصول على أو تحديد القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | يسمح بتحديد خيارات عرض ملف التعريف. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | يحصل على أو مجموعات[`NumeralFormat`](../numeralformat/) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية بشكل افتراضي. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كانت الارتباطات التشعبية الموجودة في مستند Pdf الناتج يجب أن يتم فتحها في نافذة (أو علامة تبويب) جديدة في المتصفح. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | تشير العلامة إلى ما إذا كان مطلوبًا تحسين الإخراج. إذا تم تعيين هذه العلامة للوحات القماشية المتداخلة الزائدة وتمت إزالة اللوحات الفارغة، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على`حقيقي` . الافتراضي هو`خطأ شنيع` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | يسمح بتحديد خيارات المخطط التفصيلي. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق صفحة ثابت. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | الحصول على الصفحات المراد عرضها أو تعيينها. الافتراضي هو كافة الصفحات الموجودة في المستند. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان سيتم مزج الصور الشفافة مسبقًا مع لون الخلفية السوداء أم لا. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | يحدد ما إذا كان سيتم الاحتفاظ بحقول نموذج Microsoft Word كحقول نموذج في PDF أو تحويلها إلى نص. الافتراضي هو`خطأ شنيع` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | متى`حقيقي`، إخراج تنسيقات جميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء حفظ مستند ويقبل البيانات المتعلقة بتقدم الحفظ. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقطPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | يحدد نوع الضغط الذي سيتم استخدامه لكل المحتوى النصي في المستند. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديده عبر[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استبدال خطوط TrueType Arial وTimes New Roman و Courier New وSymbol بخطوط PDF Type 1 الأساسية أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد نوع التكبير/التصغير الذي يجب تطبيقه عند فتح مستند باستخدام عارض PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | الحصول على أو تعيين قيمة تحدد عامل التكبير (بالنسبة المئوية) للمستند. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | إنشاء نسخة عميقة لهذا الكائن. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |

## أمثلة

يوضح كيفية تغيير لون الصورة مع خاصية خيارات الحفظ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// اضبط خاصية "ColorMode" على "تدرج الرمادي" لعرض جميع الصور من المستند باللونين الأبيض والأسود.
// قد يكون حجم مستند الإخراج أكبر مع هذا الإعداد.
// اضبط خاصية "ColorMode" على "عادي" لعرض جميع الصور بالألوان.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

يوضح كيفية تطبيق ضغط النص عند حفظ مستند إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "ضغط النص" على "PdfTextCompression.None" حتى لا يتم تطبيق أي منها
// الضغط على النص عندما نحفظ المستند بصيغة PDF.
// اضبط خاصية "TextCompression" على "PdfTextCompression.Flate" لتطبيق ضغط ZIP
// إلى النص عندما نحفظ المستند إلى PDF. كلما كانت الوثيقة أكبر، كلما كان التأثير أكبر.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

يوضح كيفية تحويل مستند كامل إلى PDF بثلاثة مستويات في مخطط المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل عناوين المستويات من 1 إلى 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "4" لاستبعاد كافة العناوين التي تكون مستوياتها أعلى من 4 من المخطط التفصيلي.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// إذا كان الإدخال التفصيلي يحتوي على إدخالات لاحقة بمستوى أعلى بينه وبين الإدخال التالي من نفس المستوى أو مستوى أقل،
// سيظهر سهم على يسار الإدخال. هذا الإدخال هو "مالك" العديد من هذه "الإدخالات الفرعية".
// في مستندنا، إدخالات المخطط التفصيلي من مستوى العنوان الخامس هي إدخالات فرعية لإدخال المخطط التفصيلي للمستوى الرابع الثاني،
// إدخالات مستوى العنوان الرابع والخامس هي إدخالات فرعية لإدخال المستوى الثالث الثاني، وهكذا.
// في المخطط التفصيلي، يمكننا النقر على سهم إدخال "المالك" لطي/توسيع جميع إدخالاته الفرعية.
// قم بتعيين خاصية "ExpandedOutlineLevels" على "2" لتوسيع كل مستوى العناوين 2 وإدخالات المخطط التفصيلي السفلية تلقائيًا
// وقم بطي جميع المستويات والإدخالات الثلاثة والأعلى عندما نفتح المستند.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### أنظر أيضا

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
