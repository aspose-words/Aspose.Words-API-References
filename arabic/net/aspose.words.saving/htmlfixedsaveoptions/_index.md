---
title: HtmlFixedSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفHtmlFixed التنسيق .
type: docs
weight: 4820
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفHtmlFixed التنسيق .

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان . |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix) { get; set; } | يحدد البادئة التي تمت إضافتها إلى كافة أسماء الفئات في ملف style.css. القيمة الافتراضية هي`"عذرًا"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) . القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) . |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد . |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding) { get; set; } | يحدد الترميز الذي سيتم استخدامه عند التصدير إلى HTML. القيمة الافتراضية هي`ترميز UTF8 جديد (صحيح)` (UTF-8 مع BOM) . |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss) { get; set; } | يحدد ما إذا كان يجب تضمين CSS (ورقة الأنماط المتتالية) في مستند Html. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts) { get; set; } | يحدد ما إذا كان يجب تضمين الخطوط في مستند Html بتنسيق Base64 . ملاحظة يمكن أن يؤدي إعداد هذه العلامة إلى زيادة حجم ملف Html الناتج بشكل ملحوظ. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages) { get; set; } | يحدد ما إذا كان يجب تضمين الصور في مستند Html بتنسيق Base64 . ملاحظة يمكن أن يؤدي إعداد هذه العلامة إلى زيادة حجم ملف Html الناتج بشكل كبير. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg) { get; set; } | يحدد ما إذا كان يجب تضمين موارد SVG في مستند Html. القيمة الافتراضية هي`حقيقي` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields) { get; set; } | الحصول على أو تعيين إشارة إلى ما إذا كان يتم تصدير حقول النموذج كعناصر تفاعلية (كعلامة "إدخال") بدلاً من تحويلها إلى نص أو رسومات. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat) { get; set; } | يحصل أو يحدد[`ExportFontFormat`](../exportfontformat) تستخدم لتصدير الخط. القيمة الافتراضية هيWoff . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | يسمح بتحديد خيارات عرض ملف التعريف. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | يحصل أو يحدد[`NumeralFormat`](../numeralformat) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput) { get; set; } | تشير العلامة إلى ما إذا كان مطلوبًا لتحسين الإخراج. إذا تم تعيين هذه العلامة قماشية متداخلة متكررة وتمت إزالة اللوحات الفارغة ، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق . ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على true . القيمة الافتراضية هي true . |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment) { get; set; } | يحدد المحاذاة الأفقية للصفحات في مستند HTML. القيمة الافتراضية هي`HtmlFixedHorizontalPageAlignment.Center` . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins) { get; set; } | يحدد الهوامش حول الصفحات في مستند HTML. تقاس قيمة الهوامش بالنقاط ويجب أن تكون مساوية لـ 0 أو أكبر منها . القيمة الافتراضية هي 10 نقاط . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق صفحة ثابتة. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | الحصول على الصفحات المراد عرضها أو تعيينها. الإعداد الافتراضي هو كافة الصفحات الموجودة في المستند. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم . |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback) { get; set; } | يسمح بالتحكم في كيفية حفظ الموارد (الصور والخطوط و css) عند تصدير مستند إلى تنسيق Html للصفحة الثابتة. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder) { get; set; } | يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور ، الخطوط ، css) عند تصدير مستند إلى تنسيق Html. الافتراضي هو`لا شيء` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias) { get; set; } | يحدد اسم المجلد المستخدم في إنشاء عناوين URI للصورة مكتوبة في مستند Html . الافتراضي هو`لا شيء` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately) { get; set; } | تشير العلامة إلى ما إذا كان يجب وضع قواعد CSS "@ font-face" في ملف منفصل "fontFaces.css" عندما يتم حفظ مستند مع ورقة أنماط خارجية (أي عندما[`ExportEmbeddedCss`](./exportembeddedcss) هو`خاطئة` ) . القيمة الافتراضية هي`خاطئة` ، جميع قواعد CSS مكتوبة في ملف واحد "styles.css" . |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ . يمكن فقط أن يكونHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder) { get; set; } | يحدد ما إذا كان يجب عرض الحدود حول الصفحات. القيمة الافتراضية هي`حقيقي` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت . القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts) { get; set; } | تشير العلامة إلى ما إذا كان يجب استخدام الخطوط من الجهاز الهدف لعرض المستند. إذا تم تعيين هذه العلامة على "صواب" ،[`FontFormat`](./fontformat) و[`ExportEmbeddedFonts`](./exportembeddedfonts)الخصائص ليس لها تأثير ، أيضًا[`ResourceSavingCallback`](./resourcesavingcallback) لم يتم إطلاقه من أجل الخطوط. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | لتحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |

### أمثلة

يوضح كيفية استخدام رد اتصال لطباعة URIs للموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // سيحتوي المجلد المحدد بواسطة ResourcesFolderAlias على الموارد بدلاً من ResourcesFolder.
    // يجب أن نتأكد من وجود المجلد قبل أن تضع التدفقات مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// يحسب ويطبع URIs للموارد المتضمنة بواسطة حيث يتم تحويلها إلى HTML ثابت.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // إذا قمنا بتعيين اسم مستعار للمجلد في كائن SaveOptions ، فسنكون قادرين على طباعته من هنا.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // افتراضيًا ، يستخدم "ResourceFileUri" مجلد النظام للخطوط.
                // لتجنب المشاكل في الأنظمة الأساسية الأخرى ، يجب عليك تحديد مسار الخطوط بشكل صريح.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // إذا حددنا مجلدًا في خاصية "ResourcesFolderAlias" ،
        // سنحتاج أيضًا إلى إعادة توجيه كل دفق لوضع مورده في هذا المجلد.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### أنظر أيضا

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
