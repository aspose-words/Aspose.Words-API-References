---
title: FixedPageSaveOptions Class
linktitle: FixedPageSaveOptions
articleTitle: FixedPageSaveOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.FixedPageSaveOptions فصل. يحتوي على خيارات شائعة يمكن تحديدها عند حفظ مستند بتنسيقات صفحات ثابتة PDF XPS الصور إلخ في C#.
type: docs
weight: 5020
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/
---
## FixedPageSaveOptions class

يحتوي على خيارات شائعة يمكن تحديدها عند حفظ مستند بتنسيقات صفحات ثابتة (PDF، XPS، الصور، إلخ).

لمعرفة المزيد، قم بزيارة[حدد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

```csharp
public abstract class FixedPageSaveOptions : SaveOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | الحصول على قيمة منطقية أو تعيينها تشير إلى ما إذا كان سيتم السماح بدمج الخطوط باستخدام مخططات PostScript عند حفظ تضمين خطوط TrueType في مستند. القيمة الافتراضية هي`خطأ شنيع` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض الألوان. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | الحصول على أو تعيين المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض التأثيرات ثلاثية الأبعاد. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض تأثيرات DrawML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | متى`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض كائنات الحبر (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند Html. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | الحصول على أو تحديد القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | يسمح بتحديد خيارات عرض ملف التعريف. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | يحصل على أو مجموعات[`NumeralFormat`](../numeralformat/) تستخدم لعرض الأرقام. يتم استخدام الأرقام الأوروبية بشكل افتراضي. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | تشير العلامة إلى ما إذا كان مطلوبًا تحسين الإخراج. إذا تم تعيين هذه العلامة للوحات القماشية المتداخلة الزائدة وتمت إزالة اللوحات الفارغة، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على`حقيقي` . الافتراضي هو`خطأ شنيع` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | يسمح بالتحكم في كيفية حفظ الصفحات المنفصلة عند تصدير مستند إلى تنسيق صفحة ثابت. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | الحصول على الصفحات المراد عرضها أو تعيينها. الافتراضي هو كافة الصفحات الموجودة في المستند. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | متى`حقيقي`، إخراج تنسيقات جميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء حفظ مستند ويقبل البيانات المتعلقة بتقدم الحفظ. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |

## أمثلة

يوضح كيفية عرض كل صفحة من المستند إلى صورة TIFF منفصلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // قم بتعيين خاصية "PageSet" على رقم الصفحة الأولى من
    // الذي يبدأ عرض المستند منه.
    options.PageSet = new PageSet(i);
    // تصدير الصفحة بحجم 2325 × 5325 بكسل و600 نقطة في البوصة.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

يوضح كيفية عرض صفحة واحدة من مستند إلى صورة JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// اضبط "PageSet" على "1" لتحديد الصفحة الثانية عبر
// الفهرس الصفري الذي سيتم البدء في عرض المستند منه.
options.PageSet = new PageSet(1);

// عندما نحفظ المستند بتنسيق JPEG، يعرض Aspose.Words صفحة واحدة فقط.
// ستحتوي هذه الصورة على صفحة واحدة تبدأ من الصفحة الثانية،
// والتي ستكون مجرد الصفحة الثانية من المستند الأصلي.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### أنظر أيضا

* class [SaveOptions](../saveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
