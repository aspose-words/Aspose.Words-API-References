---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.HtmlSaveOptions فصل. يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند في Html Mhtml EpubAzw3 أوMobi التنسيق في C#.
type: docs
weight: 5110
url: /ar/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند في Html ,Mhtml ,EpubAzw3 أوMobi التنسيق.

لمعرفة المزيد، قم بزيارة[حدد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ document فيHtml التنسيق. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ document فيHtml ,Mhtml ,EpubAzw3 أوMobi التنسيق. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم السماح بدمج الخطوط باستخدام مخططات PostScript عند حفظ تضمين خطوط TrueType في مستند. القيمة الافتراضية هي`خطأ شنيع` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | يحدد ما إذا كانت المسافات البادئة السلبية اليمنى واليسرى للفقرات ستتم تسويتها عند الحفظ في HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خطأ شنيع` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | تحديد بادئة تتم إضافتها إلى كافة أسماء فئات CSS. القيمة الافتراضية هي سلسلة فارغة وأسماء فئات CSS التي تم إنشاؤها لا تحتوي على بادئة مشتركة. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ أنماط CSS عند حفظ مستند بتنسيق HTML أو MHTML أو EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | يحدد المسار واسم ملف ورقة الأنماط المتتالية (CSS) الذي يتم كتابته عند تصدير مستند إلى HTML. الافتراضي هو سلسلة فارغة. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | يحدد كيفية تصدير أنماط CSS (ورقة الأنماط المتتالية) إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيInline لـ HTML/MHTML و External لـ EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | الحصول على أو تعيين المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض التأثيرات ثلاثية الأبعاد. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض تأثيرات DrawML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawML. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ أجزاء المستند عند حفظ مستند بتنسيق HTML أو EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | يحدد كيفية تقسيم المستند عند الحفظ فيهHtmlEpub أوAzw3 شكل. الافتراضي هوNone لـ HTML و HeadingParagraph لـ EPUB وAZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | يحدد الحد الأقصى لمستوى العناوين التي سيتم عندها تقسيم المستند. القيمة الافتراضية هي`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | يحدد الترميز الذي سيتم استخدامه عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`ترميز UTF8 الجديد (خطأ)` (UTF-8 بدون قائمة مكونات الصنف). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | يحدد ما إذا كان سيتم استخدام عناوين URL لـ CID (معرف المحتوى) للإشارة إلى الموارد (الصور والخطوط وCSS) المضمنة في مستندات MHTML . القيمة الافتراضية هي`خطأ شنيع` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | يحدد ما إذا كان سيتم تصدير خصائص المستند المضمنة والمخصصة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خطأ شنيع` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | يتحكم في كيفية حفظ حقول النموذج المنسدل في HTML أو MHTML. القيمة الافتراضية هي`خطأ شنيع` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | يحدد ما إذا كان يجب تصدير موارد الخطوط إلى HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | يحدد ما إذا كان يجب تضمين موارد الخطوط في HTML في ترميز Base64. الافتراضي هو`خطأ شنيع` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | متى`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | يحدد كيفية إخراج الرؤوس والتذييلات إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPerSection لـ HTML/MHTML وNone لـ EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | يحدد ما إذا كان سيتم حفظ الصور بتنسيق Base64 إلى مخرجات HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | يحدد ما إذا كان سيتم تصدير معلومات اللغة إلى HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`خطأ شنيع` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | يتحكم في كيفية إخراج تسميات القائمة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هي`خطأ شنيع` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | يحدد ما إذا كان سيتم تصدير هوامش الصفحة إلى HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`خطأ شنيع` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | يحدد ما إذا كان سيتم تصدير إعداد الصفحة إلى HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`خطأ شنيع` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ في HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`خطأ شنيع` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | يحدد ما إذا كان سيتم كتابة معلومات رحلة الذهاب والإياب عند الحفظ في HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` لـ HTML و`خطأ شنيع` لـ MHTML وEPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | يتحكم في ما إذا كان[`Shape`](../../aspose.words.drawing/shape/)يتم تحويل العقد إلى صور SVG عند حفظ إلى HTML أو MHTML أو EPUB أو AZW3. القيمة الافتراضية هي`خطأ شنيع` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | يتحكم في كيفية حفظ حقول نموذج إدخال النص في HTML أو MHTML. القيمة الافتراضية هي`خطأ شنيع` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | يحدد ما إذا كان سيتم كتابة أرقام الصفحات في جدول المحتويات عند حفظ HTML وMHTML وEPUB. القيمة الافتراضية هي`خطأ شنيع` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | يحدد ما إذا كان سيتم كتابة إعلان DOCTYPE عند الحفظ في HTML أو MHTML. متى`حقيقي` ، يكتب إعلان DOCTYPE في المستند قبل العنصر الجذر. القيمة الافتراضية هي`خطأ شنيع`. عند الحفظ في EPUB أو HTML5 (Html5 ) يتم دائمًا كتابة إعلان DOCTYPE . |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | يتحكم في موارد الخطوط التي تحتاج إلى تعيين فرعي عند الحفظ في HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الخطوط عند حفظ مستند بتنسيق HTML أو MHTML أو EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | يحدد المجلد الفعلي حيث يتم حفظ الخطوط عند تصدير مستند إلى HTML. الافتراضي هو سلسلة فارغة. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | يحدد اسم المجلد المستخدم لإنشاء معرفات URI للخط المكتوب في مستند HTML. الافتراضي هو سلسلة فارغة. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | يحدد إصدار معيار HTML الذي يجب استخدامه عند حفظ المستند إلى HTML أو MHTML. القيمة الافتراضية هيXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | يحدد دقة الإخراج للصور عند التصدير إلى HTML أو MHTML أو EPUB. الافتراضي هو`96 نقطة في البوصة` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الصور عند حفظ مستند بتنسيق HTML أو MHTML أو EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى تنسيق HTML. الافتراضي هو سلسلة فارغة. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض كائنات الحبر (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | الحصول على أو تحديد القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ ملفات التعريف عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPng ، مما يعني أن ملفات التعريف يتم عرضها على صور PNG النقطية. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | يحدد الحد الأقصى لمستوى العناوين التي يتم ملؤها في خريطة التنقل عند التصدير إلى تنسيقات EPUB، أو MOBI، أو AZW3 . القيمة الافتراضية هي`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | يتحكم في كيفية تصدير كائنات OfficeMath إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيImage . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | متى`حقيقي`، إخراج تنسيقات جميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء حفظ مستند ويقبل البيانات المتعلقة بتقدم الحفظ. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | يحدد ما إذا كان سيتم حل أسماء مجموعة الخطوط المستخدمة في المستند واستبدالها وفقًا لـ [`FontSettings`](../../aspose.words/document/fontsettings/) عند كتابتها بتنسيقات مستندة إلى HTML. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | يحدد مجلدًا فعليًا حيث يتم حفظ جميع الموارد مثل الصور والخطوط وCSS الخارجية عند تصدير document إلى HTML. الافتراضي هو سلسلة فارغة. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | يحدد اسم المجلد المستخدم لإنشاء URIs لجميع الموارد المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكونHtml ,Mhtml ,EpubAzw3 أوMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | يحدد ما إذا كان سيتم تغيير حجم الصور بواسطة Aspose.Words إلى حجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | يتحكم في كيفية تصدير عروض الجدول والصف والخلية إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

## أمثلة

يوضح كيفية تحديد المجلد لتخزين الصور المرتبطة بعد حفظها في .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// قم بتعيين خيار لتصدير حقول النموذج كنص عادي بدلاً من عناصر إدخال HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

يوضح كيفية استخدام ترميز معين عند حفظ مستند إلى .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// استخدم كائن SaveOptions لتحديد ترميز المستند الذي سنقوم بحفظه.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// بشكل افتراضي، سيحتوي مستند الإخراج .epub على جميع محتوياته في جزء HTML واحد.
// يسمح لنا معيار التقسيم بتقسيم المستند إلى عدة أجزاء بتنسيق HTML.
// سنضع المعايير لتقسيم الوثيقة إلى فقرات رأسية.
// هذا مفيد للقراء الذين لا يستطيعون قراءة ملفات HTML ذات حجم أكبر من حجم معين.
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

    // قم بإنشاء كائن "HtmlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // إذا قمنا بحفظ المستند بشكل طبيعي، فسيكون هناك مخرج HTML واحد
    // مستند يحتوي على جميع محتويات المستند المصدر.
    // قم بتعيين خاصية "DocumentSplitCriteria" على "DocumentSplitCriteria.SectionBreak" إلى
    // احفظ وثيقتنا في ملفات HTML متعددة: ملف واحد لكل قسم.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // قم بتعيين رد اتصال مخصص للخاصية "DocumentPartSavingCallback" لتغيير منطق حفظ جزء المستند.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // إذا قمنا بتحويل مستند يحتوي على صور إلى html، فسوف نحصل في النهاية على ملف html واحد يرتبط بعدة صور.
    // ستكون كل صورة على شكل ملف في نظام الملفات المحلي.
    // يوجد أيضًا رد اتصال يمكنه تخصيص الاسم وموقع نظام الملفات لكل صورة.
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
        // يمكننا الوصول إلى المستند المصدر بأكمله عبر خاصية "المستند".
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

        // فيما يلي طريقتان لتحديد المكان الذي سيحفظ فيه Aspose.Words كل جزء من المستند.
        // 1 - قم بتعيين اسم ملف لملف جزء الإخراج:
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

        // فيما يلي طريقتان لتحديد المكان الذي سيحفظ فيه Aspose.Words كل جزء من المستند.
        // 1 - قم بتعيين اسم ملف لملف الصورة الناتج:
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

* class [SaveOptions](../saveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
