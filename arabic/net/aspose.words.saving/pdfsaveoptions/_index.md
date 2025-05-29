---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات حفظ ملفات PDF من Aspose.Words لتحسين تجربة حفظ مستنداتك. خصّص الإعدادات لتحقيق أفضل جودة وأداء لملفات PDF.
type: docs
weight: 6320
url: /ar/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند فيPdf تنسيق.

لمعرفة المزيد، قم بزيارة[تحديد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند في Pdf تنسيق. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | علم يحدد ما إذا كان سيتم كتابة عوامل تحديد موضع نص إضافية أم لا. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم السماح بتضمين الخطوط مع الخطوط العريضة لـ PostScript عند تضمين خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي`خطأ شنيع` . |
| [AttachmentsEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/) { get; set; } | يحصل على قيمة تحدد كيفية تضمين المرفقات في مستند PDF أو يعينها. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | يحصل على قيمة تحدد ما إذا كان سيتم تخزين الرسومات الموضوعة في خلفية المستند أم لا. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض الألوان أو يعينها. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | يحدد مستوى التوافق مع معايير PDF للمستندات الناتجة. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | يحدد ما إذا كان سيتم تحويل مراجع الحواشي السفلية/الحواشي النهائية في القصة النصية الرئيسية إلى ارتباطات تشعبية نشطة. عند النقر فوق الارتباط التشعبي، سيقودك إلى الحاشية السفلية/الحواشي النهائية المقابلة. الإعداد الافتراضي هو`خطأ شنيع` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | يحصل على قيمة تحدد الطريقة أو يعينها[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) يتم تصديرها إلى ملف PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | يحصل على أو يعين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | يحصل على المسار إلى القالب الافتراضي (بما في ذلك اسم الملف) أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | يحصل على تفاصيل توقيع مستند PDF الناتج أو يعينها. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | علم يحدد ما إذا كان شريط عنوان النافذة يجب أن يعرض عنوان المستند المأخوذ من إدخال العنوان في قاموس معلومات المستند. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد أو يعينها. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض تأثيرات DrawingML أو يعينها. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض أشكال DrawingML أو يعينها. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | يسمح بتحديد خيارات تقليل العينة. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | يحصل على تفاصيل تشفير مستند PDF الناتج أو يعينها. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم تصدير بنية المستند أم لا. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم إنشاء علامة "Span" في بنية المستند لتصدير لغة النص أم لا. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب وضع علامة على رسم فقرة كقطعة أثرية. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | يحدد وضع تضمين الخط. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | يحدد كيفية تصدير الإشارات المرجعية في الرؤوس/التذييلات. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | يحدد كيفية تحديد مساحة اللون للصور في مستند PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | يحدد نوع الضغط الذي سيتم استخدامه لجميع الصور في المستند. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض كائنات الحبر (InkML) أو يعينها. |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | علم يشير إلى ما إذا كان سيتم تنفيذ استيفاء الصورة بواسطة قارئ متوافق. عندما`خطأ شنيع` إذا تم تحديد ذلك، فلن تتم كتابة العلم في مستند الإخراج وسيتم استخدام السلوك الافتراضي للقارئ بدلاً من ذلك. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | يحصل على قيمة تحدد جودة صور JPEG داخل مستند PDF أو يعينها. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | يحصل على القيمة أو يعينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | يسمح بتحديد خيارات عرض الملف التعريفي. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | يحصل أو يعين[`NumeralFormat`](../numeralformat/) تُستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية بشكل افتراضي. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كانت الروابط التشعبية في مستند Pdf الناتج يجب فتحها في نافذة جديدة (أو علامة تبويب) للمتصفح. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | يشير العلم إلى ما إذا كان مطلوبًا لتحسين الإخراج. إذا تم تعيين هذا العلم، تتم إزالة اللوحات المتداخلة الزائدة واللوحات الفارغة، أيضًا يتم ربط الحروف المجاورة بنفس التنسيق. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على`حقيقي` . الافتراضي هو`خطأ شنيع` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | يسمح بتحديد خيارات المخطط التفصيلي. |
| [PageLayout](../../aspose.words.saving/pdfsaveoptions/pagelayout/) { get; set; } | يحدد تخطيط الصفحة الذي سيتم استخدامه عند فتح المستند في قارئ PDF. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق الصفحة الثابتة. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | يحصل على الصفحات التي سيتم عرضها أو يعينها. الافتراضي هو كل الصفحات الموجودة في المستند. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم مزج الصور الشفافة مسبقًا مع لون الخلفية الأسود أم لا. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | يحدد ما إذا كان سيتم الحفاظ على حقول نموذج Microsoft Word كحقول نموذج في PDF أو تحويلها إلى نص. الافتراضي هو`خطأ شنيع` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | عندما`حقيقي` ، تنسيقات الإخراج الجميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء حفظ المستند وتقبل البيانات حول تقدم الحفظ. |
| [RenderChoiceFormFieldBorder](../../aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/) { get; set; } | يحدد ما إذا كان سيتم عرض حدود حقل نموذج اختيار PDF. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | يحدد نوع الضغط الذي سيتم استخدامه لجميع النصوص في المستند. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب تحديث حقول أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام التنعيم للرسم أم لا. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة الكتيبات، إذا تم تحديد ذلك عبر[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استبدال خطوط TrueType Arial وTimes New Roman و Courier New وSymbol بخطوط PDF Type 1 الأساسية أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [UseSdtTagAsFormFieldName](../../aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/) { get; set; } | يحدد ما إذا كان سيتم استخدام عنصر تحكم SDT Tag أو خاصية Id كاسم لحقل النموذج في PDF. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | يحصل على قيمة أو يعينها لتحديد نوع التكبير الذي يجب تطبيقه عند فتح مستند باستخدام عارض PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | يحصل على قيمة لتحديد عامل التكبير (بالنسب المئوية) لمستند أو يعينها. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | ينشئ نسخة طبق الأصل عميقة من هذا الكائن. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |

## أمثلة

يوضح كيفية تغيير لون الصورة باستخدام خاصية خيارات الحفظ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// قم بضبط خاصية "ColorMode" على "Grayscale" لعرض كافة الصور من المستند باللونين الأبيض والأسود.
//قد يكون حجم المستند الناتج أكبر مع هذا الإعداد.
// اضبط خاصية "ColorMode" على "Normal" لعرض كافة الصور بالألوان.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

يوضح كيفية تطبيق ضغط النص عند حفظ مستند بتنسيق PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "TextCompression" على "PdfTextCompression.None" لعدم تطبيق أي
// ضغط النص عندما نحفظ المستند بصيغة PDF.
// اضبط خاصية "TextCompression" على "PdfTextCompression.Flate" لتطبيق ضغط ZIP
// إلى نص عند حفظ المستند بصيغة PDF. كلما كان حجم المستند أكبر، كان تأثير ذلك أكبر.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

يوضح كيفية تحويل مستند كامل إلى PDF بثلاثة مستويات في مخطط المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج عناوين المستويات من 1 إلى 5.
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

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// قم بضبط خاصية "HeadingsOutlineLevels" على "4" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 4 من المخطط التفصيلي.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// إذا كان إدخال المخطط التفصيلي يحتوي على إدخالات لاحقة بمستوى أعلى بينها وبين الإدخال التالي من نفس المستوى أو المستوى الأدنى،
// سيظهر سهم على يسار المُدخلة. هذه المُدخلة هي "مالكة" العديد من هذه "المُدخلات الفرعية".
// في مستندنا، تعتبر إدخالات المخطط التفصيلي من مستوى العنوان الخامس إدخالات فرعية لإدخال المخطط التفصيلي الثاني من المستوى الرابع،
// إدخالات المستوى الرابع والخامس هي إدخالات فرعية للإدخال الثاني على المستوى الثالث، وهكذا.
// في المخطط التفصيلي، يمكننا النقر على سهم إدخال "المالك" لإخفاء/توسيع جميع إدخالاته الفرعية.
// اضبط خاصية "ExpandedOutlineLevels" على "2" لتوسيع جميع عناوين المستوى 2 وإدخالات المخطط التفصيلي السفلية تلقائيًا
// وانهيار جميع الإدخالات من المستوى 3 وما فوق عندما نفتح المستند.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### أنظر أيضا

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
