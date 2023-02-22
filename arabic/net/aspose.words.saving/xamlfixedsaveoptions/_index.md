---
title: Class XamlFixedSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.XamlFixedSaveOptions فصل. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفXamlFixed التنسيق .
type: docs
weight: 5410
url: /ar/net/aspose.words.saving/xamlfixedsaveoptions/
---
## XamlFixedSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفXamlFixed التنسيق .

```csharp
public class XamlFixedSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [XamlFixedSaveOptions](xamlfixedsaveoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) . القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) . |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد . |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | يسمح بتحديد خيارات عرض ملف التعريف. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | يحصل أو يحدد[`NumeralFormat`](../numeralformat/) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | تشير العلامة إلى ما إذا كان مطلوبًا لتحسين الإخراج. إذا تم تعيين هذه العلامة قماشية متداخلة متكررة وتمت إزالة اللوحات الفارغة ، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق . ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على "true". القيمة الافتراضية خطأ. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق صفحة ثابتة. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | الحصول على الصفحات المراد عرضها أو تعيينها. الإعداد الافتراضي هو كافة الصفحات الموجودة في المستند. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم . |
| [ResourceSavingCallback](../../aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الموارد (الصور والخطوط) عند تصدير مستند إلى تنسيق Xaml للصفحة الثابتة. |
| [ResourcesFolder](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/) { get; set; } | يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور والخطوط) عند تصدير مستند إلى تنسيق Xaml للصفحة الثابتة. الافتراضي هو`لا شيء` . |
| [ResourcesFolderAlias](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/) { get; set; } | يحدد اسم المجلد المستخدم في إنشاء عناوين URI للصورة مكتوبة في مستند Xaml بصفحة ثابتة. الافتراضي هو`لا شيء` . |
| override [SaveFormat](../../aspose.words.saving/xamlfixedsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ . يمكن فقط أن يكونXamlFixed . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت . القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | لتحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |

### أمثلة

يوضح كيفية طباعة URIs للموارد المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى نموذج ثابت .xaml.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // قم بإنشاء كائن "XamlFixedSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية حفظ المستند بتنسيق حفظ XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // استخدم خاصية "ResourcesFolder" لتعيين مجلد في نظام الملفات المحلي فيه
    // Aspose.Words ستحفظ جميع الموارد المرتبطة بالمستند ، مثل الصور والخطوط.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // استخدم خاصية "ResourcesFolderAlias" لاستخدام هذا المجلد
    // عند إنشاء عناوين URI للصورة بدلاً من اسم مجلد الموارد.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // سيحتاج المجلد المحدد بواسطة "ResourcesFolderAlias" إلى احتواء الموارد بدلاً من "ResourcesFolder".
    // يجب أن نتأكد من وجود المجلد قبل أن تتمكن تدفقات رد الاتصال من وضع مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// يحسب ويطبع URIs للموارد التي تم إنشاؤها أثناء التحويل إلى .xaml ثابت.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // إذا حددنا اسمًا مستعارًا لمجلد الموارد ، فسنحتاج أيضًا
        // لإعادة توجيه كل دفق لوضع مورده في مجلد الاسم المستعار.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### أنظر أيضا

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


