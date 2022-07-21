---
title: HtmlSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفHtml  Mhtml أوEpub التنسيق .
type: docs
weight: 4850
url: /ar/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفHtml ، Mhtml أوEpub التنسيق .

```csharp
public class HtmlSaveOptions : SaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions#constructor)() | تهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ document فيHtml التنسيق . |
| [HtmlSaveOptions](htmlsaveoptions#constructor_1)(SaveFormat) | تهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ document فيHtml وMhtml أوEpub التنسيق . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent) { get; set; } | يحدد ما إذا كانت المسافات البادئة اليمنى واليسرى السالبة للفقرات طبيعية عند الحفظ بتنسيق HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خاطئة` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix) { get; set; } | يحدد بادئة تمت إضافتها إلى جميع أسماء فئات CSS . القيمة الافتراضية هي سلسلة فارغة ولا تحتوي أسماء فئات CSS المُنشأة على بادئة مشتركة. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ أنماط CSS عند حفظ مستند بتنسيق HTML أو MHTML أو EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename) { get; set; } | يحدد المسار واسم ملف ورقة الأنماط المتتالية (CSS) المكتوب عند تصدير document إلى HTML. الافتراضي هو سلسلة فارغة. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype) { get; set; } | يحدد كيفية تصدير أنماط CSS (ورقة الأنماط المتتالية) إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيInline لـ HTML / MHTML و External لـ EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) . القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) . |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد . |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ أجزاء المستند عند حفظ المستند بتنسيق HTML أو EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria) { get; set; } | يحدد كيفية تقسيم المستند عند الحفظHtml أوEpub صيغة. الافتراضي هوNone لـ HTML و HeadingParagraph لـ EPUB. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel) { get; set; } | يحدد المستوى الأقصى للعناوين التي يتم عندها تقسيم المستند. القيمة الافتراضية هي`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding) { get; set; } | يحدد الترميز المراد استخدامه عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`ترميز UTF8 جديد (خطأ)` (UTF-8 بدون BOM) . |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel) { get; set; } | يحدد المستوى الأقصى للعناوين التي يتم ملؤها في خريطة التنقل عند التصدير إلى تنسيق IDPF EPUB . القيمة الافتراضية هي`3` . |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources) { get; set; } | يحدد ما إذا كان سيتم استخدام عناوين URL لـ CID (معرف المحتوى) للإشارة إلى الموارد (الصور والخطوط و CSS) المضمنة في مستندات MHTML . القيمة الافتراضية هي`خاطئة` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties) { get; set; } | يحدد ما إذا كان سيتم تصدير خصائص المستند المضمنة والمخصصة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خاطئة` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext) { get; set; } | يتحكم في كيفية حفظ حقول النموذج المنسدل في HTML أو MHTML . القيمة الافتراضية هي`خاطئة` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources) { get; set; } | يحدد ما إذا كان يجب تصدير موارد الخط إلى HTML أو MHTML أو EPUB . الافتراضي هو`خاطئة` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64) { get; set; } | يحدد ما إذا كان يجب تضمين موارد الخطوط في HTML في ترميز Base64 . الافتراضي هو`خاطئة` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode) { get; set; } | يحدد كيفية إخراج الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPerSection لـ HTML / MHTML وNone لـ EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64) { get; set; } | يحدد ما إذا كانت الصور سيتم حفظها بتنسيق Base64 لإخراج HTML أو MHTML أو EPUB. الافتراضي هو`خاطئة` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation) { get; set; } | يحدد ما إذا كان سيتم تصدير معلومات اللغة إلى HTML أو MHTML أو EPUB. الافتراضي هو`خاطئة` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels) { get; set; } | يتحكم في كيفية إخراج تسميات القوائم إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages) { get; set; } | يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هي`خاطئة` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins) { get; set; } | يحدد ما إذا كان سيتم تصدير هوامش الصفحة إلى HTML أو MHTML أو EPUB . الافتراضي هو`خاطئة` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup) { get; set; } | يحدد ما إذا كان إعداد الصفحة سيتم تصديره إلى HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`خاطئة` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize) { get; set; } | يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ بتنسيق HTML أو MHTML أو EPUB . الافتراضي هو`خاطئة` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation) { get; set; } | يحدد ما إذا كان سيتم كتابة معلومات الرحلة ذهابًا وإيابًا عند الحفظ بتنسيق HTML أو MHTML أو EPUB . القيمة الافتراضية هي`حقيقي` لـ HTML و`خاطئة` لـ MHTML و EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg) { get; set; } | يتحكم في ما إذا كان[`Shape`](../../aspose.words.drawing/shape) يتم تحويل العقد إلى صور SVG عند الحفظ بتنسيق HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خاطئة` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext) { get; set; } | يتحكم في كيفية حفظ حقول نموذج إدخال النص في HTML أو MHTML. القيمة الافتراضية هي`خاطئة` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers) { get; set; } | يحدد ما إذا كان سيتم كتابة أرقام الصفحات في جدول المحتويات عند حفظ HTML و MHTML و EPUB. القيمة الافتراضية هي`خاطئة` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional) { get; set; } | يحدد ما إذا كان سيتم كتابة إعلان DOCTYPE عند الحفظ بتنسيق HTML أو MHTML.`حقيقي` ، يكتب إعلان DOCTYPE في المستند قبل عنصر الجذر. القيمة الافتراضية هي`خاطئة`. عند الحفظ في EPUB أو HTML5 (Html5 ) يتم كتابة إعلان DOCTYPE دائمًا. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold) { get; set; } | يتحكم في تحديد موارد الخط التي تحتاج إلى تعيين عند الحفظ بتنسيق HTML أو MHTML أو EPUB . الإعداد الافتراضي هو`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ الخطوط عند حفظ المستند بتنسيق HTML أو MHTML أو EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder) { get; set; } | يحدد المجلد الفعلي حيث يتم حفظ الخطوط عند تصدير مستند إلى HTML. الافتراضي هو عبارة عن سلسلة فارغة. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias) { get; set; } | يحدد اسم المجلد المستخدم في إنشاء عناوين URI للخط مكتوبة في مستند HTML. الافتراضي هو عبارة عن سلسلة فارغة. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion) { get; set; } | يحدد إصدار معيار HTML الذي يجب استخدامه عند حفظ المستند بتنسيق HTML أو MHTML . القيمة الافتراضية هيXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution) { get; set; } | يحدد دقة الإخراج للصور عند التصدير إلى HTML أو MHTML أو EPUB. الافتراضي هو`96 نقطة في البوصة` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ الصور عند حفظ المستند بتنسيق HTML أو MHTML أو EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder) { get; set; } | يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى تنسيق HTML. الافتراضي هو عبارة عن سلسلة فارغة. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias) { get; set; } | يحدد اسم المجلد المستخدم في إنشاء عناوين URI للصورة مكتوبة في مستند HTML. الافتراضي هو عبارة عن سلسلة فارغة. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat) { get; set; } | يحدد التنسيق الذي يتم حفظ ملفات التعريف به عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPng ، مما يعني أنه يتم تقديم ملفات التعريف إلى صور PNG نقطية. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode) { get; set; } | يتحكم في كيفية تصدير كائنات OfficeMath إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`HtmlOfficeMathOutputMode.Image` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم . |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames) { get; set; } | يحدد ما إذا كانت أسماء عائلة الخط المستخدمة في المستند سيتم حلها واستبدالها وفقًا لـ [`FontSettings`](../../aspose.words/document/fontsettings) عند كتابتها في تنسيقات تستند إلى HTML. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder) { get; set; } | يحدد مجلدًا ماديًا حيث يتم حفظ جميع الموارد مثل الصور والخطوط و CSS الخارجية عند تصدير document إلى HTML. الافتراضي هو عبارة عن سلسلة فارغة. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias) { get; set; } | يحدد اسم المجلد المستخدم لإنشاء URIs لجميع الموارد المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا . يمكن أن يكونHtml وMhtml أوEpub . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize) { get; set; } | يحدد ما إذا كان يتم قياس الصور بواسطة Aspose.Words لحجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode) { get; set; } | يتحكم في كيفية تصدير عرض الجدول والصف والخلية إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت . القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

### أمثلة

يوضح كيفية تحديد مجلد لتخزين الصور المرتبطة بعد الحفظ في .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// تعيين خيار لتصدير حقول النموذج كنص عادي بدلاً من عناصر إدخال HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

يوضح كيفية استخدام ترميز معين عند حفظ مستند في epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// استخدم كائن SaveOptions لتحديد ترميز المستند الذي سنقوم بحفظه.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// بشكل افتراضي ، سيكون لمستند الإخراج .epub جميع محتوياته في جزء HTML واحد.
// يسمح لنا معيار الانقسام بتقسيم المستند إلى عدة أجزاء بتنسيق HTML.
// سنضع المعايير لتقسيم الوثيقة إلى فقرات عنوان.
// هذا مفيد للقراء الذين لا يستطيعون قراءة ملفات HTML أكثر من حجم معين.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// حدد أننا نريد تصدير خصائص المستند.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

يوضح كيفية تقسيم مستند إلى أجزاء وحفظها.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // قم بإنشاء كائن "HtmlFixedSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // إذا حفظنا المستند بشكل طبيعي ، فسيكون هناك ناتج HTML واحد
    // مستند بجميع محتويات المستند المصدر.
    // تعيين خاصية "DocumentSplitCriteria" إلى "DocumentSplitCriteria.SectionBreak" إلى
    // احفظ وثيقتنا في عدة ملفات HTML: واحد لكل قسم.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // تعيين رد اتصال مخصص لخاصية "DocumentPartSavingCallback" لتغيير منطق حفظ جزء المستند.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // إذا قمنا بتحويل مستند يحتوي على صور إلى html ، فسننتهي بملف html واحد يرتبط بعدة صور.
    // ستكون كل صورة في شكل ملف في نظام الملفات المحلي.
    // يوجد أيضًا رد اتصال يمكنه تخصيص اسم وموقع نظام الملفات لكل صورة.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// يعين أسماء ملفات مخصصة لمستندات الإخراج التي تقوم عملية الحفظ بتقسيم المستند إليها.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // يمكننا الوصول إلى المستند المصدر بالكامل عبر خاصية "المستند".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // فيما يلي طريقتان لتحديد مكان حفظ Aspose.Words كل جزء من المستند.
        // 1 - حدد اسم ملف لملف جزء الإخراج:
        args.DocumentPartFileName = partFileName;

        // 2 - إنشاء دفق مخصص لملف جزء الإخراج:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// يعين أسماء ملفات مخصصة لملفات الصور التي ينشئها تحويل HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // فيما يلي طريقتان لتحديد مكان حفظ Aspose.Words كل جزء من المستند.
        // 1 - حدد اسم ملف لملف الصورة الناتج:
        args.ImageFileName = imageFileName;

        // 2 - إنشاء دفق مخصص لملف الصورة الناتج:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### أنظر أيضا

* class [SaveOptions](../saveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
