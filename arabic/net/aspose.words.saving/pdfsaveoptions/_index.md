---
title: PdfSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفPdf التنسيق .
type: docs
weight: 5240
url: /ar/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفPdf التنسيق .

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions)() | تهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند في Pdf التنسيق . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning) { get; set; } | علامة تحدد ما إذا كنت تريد كتابة عوامل تحديد مواقع نصية إضافية أم لا. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان . |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance) { get; set; } | يحدد مستوى التوافق مع معايير PDF لمستندات الإخراج. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks) { get; set; } | يحدد ما إذا كان سيتم تحويل مراجع الحواشي السفلية / التعليقات الختامية في القصة النصية الرئيسية إلى ارتباطات تشعبية نشطة.`خاطئة` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport) { get; set; } | الحصول على أو تعيين قيمة تحدد الطريقة[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties) يتم تصديرها إلى ملف PDF . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) . القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) . |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails) { get; set; } | الحصول على أو تعيين التفاصيل الخاصة بتوقيع مستند PDF الناتج. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle) { get; set; } | علامة تحدد ما إذا كان يجب أن يعرض شريط عنوان النافذة عنوان المستند المأخوذ من إدخال العنوان لقاموس معلومات المستند. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد . |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions) { get; set; } | يسمح بتحديد خيارات الاختزال . |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts) { get; set; } | يتحكم في كيفية دمج الخطوط في مستندات PDF الناتجة. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails) { get; set; } | الحصول على أو تعيين التفاصيل الخاصة بتشفير مستند PDF الناتج. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم تصدير بنية المستند أم لا. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم إنشاء علامة "امتداد" في بنية المستند لتصدير لغة النص أم لا. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode) { get; set; } | يحدد وضع دمج الخط. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode) { get; set; } | يحدد كيفية تصدير الإشارات المرجعية في الرؤوس / التذييلات . |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode) { get; set; } | يحدد كيفية اختيار مساحة اللون للصور في مستند PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression) { get; set; } | يحدد نوع الضغط الذي سيتم استخدامه لجميع الصور في المستند. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages) { get; set; } | علامة تشير إلى ما إذا كان يجب إجراء استكمال الصورة بواسطة قارئ مطابق. متى`خاطئة` لم يتم تحديد العلامة إلى مستند الإخراج و يتم استخدام السلوك الافتراضي للقارئ بدلاً من ذلك. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality) { get; set; } | الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | يسمح بتحديد خيارات عرض ملف التعريف. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | يحصل أو يحدد[`NumeralFormat`](../numeralformat) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كانت الارتباطات التشعبية الموجودة في ملف PDF الناتج document مفروضة على الفتح في نافذة (أو علامة تبويب) جديدة من المستعرض. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | تشير العلامة إلى ما إذا كان مطلوبًا لتحسين الإخراج. إذا تم تعيين هذه العلامة قماشية متداخلة متكررة وتمت إزالة اللوحات الفارغة ، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق . ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على "true". القيمة الافتراضية خطأ. |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions) { get; } | يسمح بتحديد خيارات المخطط التفصيلي . |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode) { get; set; } | يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق صفحة ثابتة. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | الحصول على الصفحات المراد عرضها أو تعيينها. الإعداد الافتراضي هو كافة الصفحات الموجودة في المستند. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم المزج المسبق للصور الشفافة بلون خلفية أسود أم لا. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields) { get; set; } | يحدد ما إذا كان سيتم الاحتفاظ بحقول نموذج Microsoft Word كحقول نموذج في PDF أو تحويلها إلى نص. الافتراضي هو`خاطئة` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم . |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ . يمكن فقط أن يكونPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression) { get; set; } | يحدد نوع الضغط الذي سيتم استخدامه لجميع المحتويات النصية في المستند. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت . القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة كتيب ، إذا تم تحديده عبر[`MultiplePages`](../../aspose.words/pagesetup/multiplepages) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استبدال خطوط TrueType Arial و Times New Roman و Courier New و Symbol بخطوط PDF Type 1 الأساسية. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior) { get; set; } | الحصول على أو تعيين قيمة تحدد نوع التكبير / التصغير الذي يجب تطبيقه عند فتح مستند باستخدام عارض PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor) { get; set; } | الحصول على أو تعيين قيمة تحدد عامل التكبير / التصغير (بالنسبة المئوية) لمستند. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone)() | لإنشاء نسخة عميقة من هذا الكائن . |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | لتحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |

### أمثلة

يوضح كيفية تغيير لون الصورة باستخدام خاصية خيارات الحفظ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
// اضبط خاصية "ColorMode" على "Grayscale" لعرض كل الصور من المستند بالأبيض والأسود.
// قد يكون حجم المستند الناتج أكبر مع هذا الإعداد.
// اضبط خاصية "ColorMode" على "عادي" لتقديم كل الصور بالألوان.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

يوضح كيفية تطبيق ضغط النص عند حفظ مستند في PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "TextCompression" على "PdfTextCompression.None" لعدم تطبيق أي منها
// الضغط على النص عندما نحفظ المستند في PDF.
// اضبط خاصية "TextCompression" على "PdfTextCompression.Flate" لتطبيق ضغط ZIP
// إلى النص عندما نحفظ المستند في PDF. كلما زاد حجم المستند ، زاد تأثير ذلك.
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

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي ، وهو جدول محتويات يسرد العناوين في نص المستند.
// سيأخذنا النقر فوق إدخال في هذا المخطط التفصيلي إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "4" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 4 من المخطط التفصيلي.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// إذا كان إدخال المخطط التفصيلي يحتوي على إدخالات لاحقة من مستوى أعلى بين نفسه والإدخال التالي من نفس المستوى أو المستوى الأدنى ،
// سيظهر سهم على يسار الإدخال. هذا الإدخال هو "مالك" العديد من هذه "الإدخالات الفرعية".
// في وثيقتنا ، إدخالات المخطط التفصيلي من مستوى العنوان الخامس هي إدخالات فرعية لإدخال المخطط التفصيلي الثاني من المستوى الرابع ،
 // تعد إدخالات مستوى العنوان الرابع والخامس إدخالات فرعية لإدخال المستوى الثالث الثاني ، وما إلى ذلك.
// في المخطط التفصيلي ، يمكننا النقر فوق سهم إدخال "المالك" لطي / توسيع جميع إدخالاته الفرعية.
// قم بتعيين خاصية "ExpandedOutlineLevels" على "2" لتوسيع كل مستوى العنوان 2 وإدخالات المخطط التفصيلي السفلية تلقائيًا
 // وطي كل المستويات والإدخالات 3 وأعلى عندما نفتح المستند.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### أنظر أيضا

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
