---
title: HtmlFixedSaveOptions Class
linktitle: HtmlFixedSaveOptions
articleTitle: HtmlFixedSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.Saving.HtmlFixedSave لتحسين تجربة حفظ مستنداتك. خصّص الإعدادات للحصول على أفضل نتائج بتنسيق HtmlFixed.
type: docs
weight: 5830
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند فيHtmlFixed تنسيق.

لمعرفة المزيد، قم بزيارة[تحديد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم السماح بتضمين الخطوط مع الخطوط العريضة لـ PostScript عند تضمين خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي`خطأ شنيع` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض الألوان أو يعينها. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | يحدد البادئة التي تتم إضافتها إلى جميع أسماء الفئات في ملف style.css. القيمة الافتراضية هي`"أوه"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | يحصل على أو يعين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | يحصل على المسار إلى القالب الافتراضي (بما في ذلك اسم الملف) أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد أو يعينها. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض تأثيرات DrawingML أو يعينها. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض أشكال DrawingML أو يعينها. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | يحدد الترميز الذي سيتم استخدامه عند التصدير إلى HTML. القيمة الافتراضية هي`ترميز UTF8 الجديد (true)` (UTF-8 مع BOM). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | يحدد ما إذا كان يجب تضمين CSS (ورقة الأنماط المتتالية) في مستند HTML. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | يحدد ما إذا كان يجب تضمين الخطوط في مستند HTML بتنسيق Base64. لاحظ أن تعيين هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف HTML الناتج. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | يحدد ما إذا كان يجب تضمين الصور في مستند HTML بتنسيق Base64. لاحظ أن تعيين هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف HTML الناتج. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | يحدد ما إذا كان يجب تضمين موارد SVG في مستند HTML. القيمة الافتراضية هي`حقيقي` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | يحصل على أو يعين مؤشرًا حول ما إذا كانت حقول النموذج يتم تصديرها كعناصر interactive (كعلامة "إدخال") بدلاً من تحويلها إلى نص أو رسومات. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | يحصل أو يعين[`ExportFontFormat`](../exportfontformat/) يستخدم لتصدير الخط. القيمة الافتراضية هيWoff . |
| [IdPrefix](../../aspose.words.saving/htmlfixedsaveoptions/idprefix/) { get; set; } | يحدد بادئة يتم إضافتها مسبقًا إلى جميع معرفات العناصر المولدة في المستند الناتج. القيمة الافتراضية هي null ولا يتم إضافة أي بادئة مسبقًا. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض كائنات الحبر (InkML) أو يعينها. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | يحصل على قيمة تحدد جودة صور JPEG داخل مستند HTML أو يعينها. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | يحصل على القيمة أو يعينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | يسمح بتحديد خيارات عرض الملف التعريفي. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | يحصل أو يعين[`NumeralFormat`](../numeralformat/) تُستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية بشكل افتراضي. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | يشير العلم إلى ما إذا كان مطلوبًا لتحسين الإخراج. إذا تم تعيين هذا العلم، تتم إزالة اللوحات المتداخلة الزائدة واللوحات الفارغة، يتم أيضًا ربط الحروف المجاورة بنفس التنسيق. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على`حقيقي` . الافتراضي هو`حقيقي` . |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | يحدد المحاذاة الأفقية للصفحات في مستند HTML. القيمة الافتراضية هيCenter . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | يحدد الهوامش حول الصفحات في مستند HTML. يتم قياس قيمة الهوامش بالنقاط ويجب أن تكون مساوية أو أكبر من 0. القيمة الافتراضية هي 10 نقاط. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق الصفحة الثابتة. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | يحصل على الصفحات التي سيتم عرضها أو يعينها. الافتراضي هو كل الصفحات الموجودة في المستند. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | عندما`حقيقي` ، تنسيقات الإخراج الجميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء حفظ المستند وتقبل البيانات حول تقدم الحفظ. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/) { get; set; } | يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. الافتراضي هو`خطأ شنيع` . |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الموارد (الصور والخطوط وCSS) عند تصدير مستند إلى تنسيق HTML لصفحة ثابتة. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | يحدد المجلد الفعلي الذي يتم حفظ الموارد فيه (الصور والخطوط وCSS) عند تصدير مستند إلى تنسيق Html. الافتراضي هو`باطل` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند HTML. الافتراضي هو`باطل` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | يشير العلم إلى ما إذا كان يجب وضع قواعد CSS "@font-face" في ملف منفصل "fontFaces.css" عند حفظ مستند باستخدام جدول أنماط خارجي (أي عندما[`ExportEmbeddedCss`](./exportembeddedcss/) هو`خطأ شنيع` ). القيمة الافتراضية هي`خطأ شنيع` ، تتم كتابة جميع قواعد CSS في ملف واحد "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | يحدد ما إذا كان يجب إظهار الحدود حول الصفحات. الافتراضي هو`حقيقي` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب تحديث حقول أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام التنعيم للرسم أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | يشير العلم إلى ما إذا كان يجب استخدام الخطوط من الجهاز المستهدف لعرض المستند. إذا تم تعيين هذا العلم على`حقيقي` ،[`FontFormat`](./fontformat/) و[`ExportEmbeddedFonts`](./exportembeddedfonts/) الخصائص ليس لها تأثير، أيضًا[`ResourceSavingCallback`](./resourcesavingcallback/) لا يتم تشغيله للخطوط. الافتراضي هو`خطأ شنيع` . |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |

## أمثلة

يوضح كيفية استخدام معاودة الاتصال لطباعة عناوين URI للموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

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
    // يتعين علينا التأكد من وجود المجلد قبل أن تتمكن التدفقات من وضع مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// يقوم بحساب وطباعة عناوين URI للموارد المضمنة أثناء تحويلها إلى HTML ثابت.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // إذا قمنا بتعيين اسم مستعار للمجلد في كائن SaveOptions، فسوف نتمكن من طباعته من هنا.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // بشكل افتراضي، يستخدم 'ResourceFileUri' مجلد النظام للخطوط.
                // لتجنب المشاكل في المنصات الأخرى، يجب عليك تحديد المسار للخطوط بشكل صريح.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // إذا قمنا بتحديد مجلد في خاصية "ResourcesFolderAlias"،
        // سوف نحتاج أيضًا إلى إعادة توجيه كل مجرى لوضع موارده في هذا المجلد.
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

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
