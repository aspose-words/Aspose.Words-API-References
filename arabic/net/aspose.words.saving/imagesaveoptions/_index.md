---
title: ImageSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: يسمح بتحديد خيارات إضافية عند عرض صفحات المستند أو الأشكال على الصور.
type: docs
weight: 4970
url: /ar/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

يسمح بتحديد خيارات إضافية عند عرض صفحات المستند أو الأشكال على الصور.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(SaveFormat) | تهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ الصور المعروضة في Tiff وPng وBmp ، Emf وJpeg أوSvg التنسيق . Png وBmp وJpeg أوSvg التنسيق . |

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
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | يسمح بتحديد وضع العرض والجودة لملفGraphics الكائن . |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | الحصول على أو تعيين الدقة الأفقية للصور التي تم إنشاؤها ، بالنقاط في البوصة . |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | الحصول على أو ضبط سطوع الصور التي تم إنشاؤها. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | الحصول على أو تحديد وضع الألوان للصور التي تم إنشاؤها. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | الحصول على أو تعيين التباين للصور التي تم إنشاؤها. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | الحصول على أو تعيين قيمة تحدد جودة صور JPEG التي تم إنشاؤها. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | يسمح بتحديد كيفية معالجة ملفات التعريف في الإخراج المعروض. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | يحصل أو يحدد[`NumeralFormat`](../numeralformat/) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية افتراضيًا. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | تشير العلامة إلى ما إذا كان مطلوبًا لتحسين الإخراج. إذا تم تعيين هذه العلامة قماشية متداخلة متكررة وتمت إزالة اللوحات الفارغة ، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق . ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على "true". القيمة الافتراضية خطأ. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق صفحة ثابتة. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | الحصول على الصفحات المراد عرضها أو تعيينها. الإعداد الافتراضي هو كافة الصفحات الموجودة في المستند. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | الحصول على أو تعيين لون الخلفية (الورق) للصور التي تم إنشاؤها. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | الحصول على أو تحديد تنسيق البكسل للصور التي تم إنشاؤها. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم . |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | يضبط الدقة الأفقية والرأسية للصور التي تم إنشاؤها ، بالنقاط في البوصة . |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم به حفظ صفحات المستند أو الأشكال المعروضة إذا تم استخدام كائن خيارات الحفظ هذا.Tiff وPng وBmp ، Jpeg أو ناقلEmf وSvg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | الحصول على أو تحديد عامل التكبير / التصغير للصور التي تم إنشاؤها. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | الحصول على أو تعيين الحد الذي يحدد القيمة لخطأ الترميز الثنائي في طريقة Floyd-Steinberg.[`ImageBinarizationMethod`](../imagebinarizationmethod/) هي ImageBinarizationMethod.FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | الحصول على أو تعيين الطريقة المستخدمة أثناء تحويل الصور إلى تنسيق 1 bpp عندما[`SaveFormat`](./saveformat/) هو SaveFormat.Tiff and [`TiffCompression`](./tiffcompression/) يساوي TiffCompression.Ccitt3 أو TiffCompression.Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | الحصول على أو تحديد نوع الضغط المراد تطبيقه عند حفظ الصور المُنشأة بتنسيق TIFF. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت . القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام عارض GDI + أو Aspose.Words ملف تعريف عند الحفظ في EMF . |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | الحصول على أو تعيين الدقة الرأسية للصور التي تم إنشاؤها ، بالنقاط في البوصة . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | لإنشاء نسخة عميقة من هذا الكائن . |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | لتحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |

### أمثلة

يجسد صفحة من مستند Word في صورة ذات خلفية شفافة أو ملونة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// اضبط خاصية "PaperColor" على لون شفاف لتطبيق شفاف
// خلفية المستند أثناء تحويله إلى صورة.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// اضبط خاصية "PaperColor" على لون معتم لتطبيق هذا اللون
// كخلفية للوثيقة عندما نعرضها على صورة.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

يوضح كيفية تكوين الضغط أثناء حفظ مستند بتنسيق JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// اضبط خاصية "JpegQuality" على "10" لاستخدام ضغط أقوى عند تقديم المستند.
// سيؤدي ذلك إلى تقليل حجم ملف المستند ، لكن الصورة ستعرض المزيد من عناصر الضغط البارزة.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// اضبط خاصية "JpegQuality" على "100" لاستخدام ضغط أضعف عند تمزيق المستند.
// سيؤدي ذلك إلى تحسين جودة الصورة على حساب زيادة حجم الملف.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

يوضح كيفية تحديد دقة أثناء تقديم مستند إلى PNG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
            // لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // اضبط خاصية "Resolution" على "72" لتقديم المستند بدقة 72 نقطة في البوصة.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // اضبط خاصية "Resolution" على "300" لتقديم المستند بدقة 300 نقطة في البوصة.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

### أنظر أيضا

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
