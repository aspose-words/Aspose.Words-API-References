---
title: SvgSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفSvg التنسيق ._ x000d_
type: docs
weight: 5320
url: /ar/net/aspose.words.saving/svgsaveoptions/
---
## SvgSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفSvg التنسيق ._ x000d_

```csharp
public class SvgSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [SvgSaveOptions](svgsaveoptions)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان ._ x000d_ |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) ._ x000d_ القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) ._ x000d_ |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد ._ x000d_ |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [ExportEmbeddedImages](../../aspose.words.saving/svgsaveoptions/exportembeddedimages) { get; set; } | تم تحديد ما إذا كان يجب تضمين الصور في مستند SVG كـ base64. ملاحظة يمكن أن يؤدي تعيين هذه العلامة إلى زيادة حجم ملف SVG الناتج بشكل ملحوظ. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [FitToViewPort](../../aspose.words.saving/svgsaveoptions/fittoviewport) { get; set; } | يحدد ما إذا كان يجب أن يملأ SVG الناتج منطقة منفذ العرض المتاحة (نافذة المتصفح أو الحاوية) ._ x000d_ عند التعيين على العرض الحقيقي وارتفاع الناتج SVG يتم تعيينه على 100٪. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | يسمح بتحديد خيارات عرض ملف التعريف. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | يحصل أو يحدد[`NumeralFormat`](../numeralformat) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | تشير العلامة إلى ما إذا كان مطلوبًا لتحسين الإخراج. _ x000d_ إذا تم تعيين هذه العلامة قماشية متداخلة متكررة وتمت إزالة اللوحات الفارغة ، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق . ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على "true". القيمة الافتراضية خطأ. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق صفحة ثابتة. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | الحصول على الصفحات المراد عرضها أو تعيينها. الإعداد الافتراضي هو كافة الصفحات الموجودة في المستند. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم ._ x000d_ |
| [ResourceSavingCallback](../../aspose.words.saving/svgsaveoptions/resourcesavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ الموارد (الصور) عند تصدير مستند إلى تنسيق SVG. |
| [ResourcesFolder](../../aspose.words.saving/svgsaveoptions/resourcesfolder) { get; set; } | يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور) عند تصدير مستند إلى تنسيق Svg . الافتراضي هو`لا شيء` . |
| [ResourcesFolderAlias](../../aspose.words.saving/svgsaveoptions/resourcesfolderalias) { get; set; } | يحدد اسم المجلد المستخدم لتكوين URIs للصور المكتوبة في مستند SVG . الافتراضي هو`لا شيء` . |
| override [SaveFormat](../../aspose.words.saving/svgsaveoptions/saveformat) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ . يمكن فقط أن يكونSvg . |
| [ShowPageBorder](../../aspose.words.saving/svgsaveoptions/showpageborder) { get; set; } | التحكم في إضافة حد إلى مخطط الصفحة. الإعداد الافتراضي هو`حقيقي` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [TextOutputMode](../../aspose.words.saving/svgsaveoptions/textoutputmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض النص بتنسيق SVG. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت ._ x000d_ القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | لتحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |

### أمثلة

يوضح كيفية معالجة وطباعة URIs للموارد المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// يحسب ويطبع URIs للموارد المتضمنة بواسطة عندما يتم تحويلها إلى .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### أنظر أيضا

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
