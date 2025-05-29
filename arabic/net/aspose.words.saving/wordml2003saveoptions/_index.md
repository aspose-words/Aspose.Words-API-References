---
title: WordML2003SaveOptions Class
linktitle: WordML2003SaveOptions
articleTitle: WordML2003SaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.WordML2003SaveOptions لتحسين تجربة حفظ المستندات بتنسيق WordML باستخدام خيارات قابلة للتخصيص.
type: docs
weight: 6480
url: /ar/net/aspose.words.saving/wordml2003saveoptions/
---
## WordML2003SaveOptions class

يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند فيWordML تنسيق.

لمعرفة المزيد، قم بزيارة[تحديد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

```csharp
public class WordML2003SaveOptions : SaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [WordML2003SaveOptions](wordml2003saveoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم السماح بتضمين الخطوط مع الخطوط العريضة لـ PostScript عند تضمين خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي`خطأ شنيع` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | يحصل على أو يعين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | يحصل على المسار إلى القالب الافتراضي (بما في ذلك اسم الملف) أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد أو يعينها. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض تأثيرات DrawingML أو يعينها. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض أشكال DrawingML أو يعينها. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض كائنات الحبر (InkML) أو يعينها. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | يحصل على القيمة أو يعينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | عندما`حقيقي` ، تنسيقات الإخراج الجميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء حفظ المستند وتقبل البيانات حول تقدم الحفظ. |
| override [SaveFormat](../../aspose.words.saving/wordml2003saveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاWordML . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب تحديث حقول أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام التنعيم للرسم أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

## ملاحظات

في الوقت الحالي يوفر فقط[`SaveFormat`](./saveformat/) الممتلكات، ولكن في المستقبل قد يتم إضافة خيارات أخرى.

## أمثلة

يوضح كيفية إدارة تحسين الذاكرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "WordML2003SaveOptions" لتمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى تنسيق حفظ WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

// اضبط علامة "MemoryOptimization" على "true" لتقليل استهلاك الذاكرة
// أثناء عملية حفظ المستند على حساب وقت حفظ أطول.
// اضبط علامة "MemoryOptimization" على "false" لحفظ المستند بشكل طبيعي.
options.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.MemoryOptimization.xml", options);
```

يوضح كيفية إدارة المحتوى الخام للمستند الناتج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "WordML2003SaveOptions" لتمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى تنسيق حفظ WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// اضبط خاصية "PrettyFormat" على "true" لتطبيق مسافة بادئة لأحرف الجدولة و
//أسطر جديدة لجعل محتوى المستند الناتج الخام أسهل للقراءة.
// اضبط خاصية "PrettyFormat" على "false" لحفظ محتوى المستند الخام في نص واحد مستمر.
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");
string newLine = Environment.NewLine;

if (prettyFormat)
    Assert.True(fileContents.Contains(
        $"<o:DocumentProperties>{newLine}\t\t" +
            $"<o:Revision>1</o:Revision>{newLine}\t\t" +
            $"<o:TotalTime>0</o:TotalTime>{newLine}\t\t" +
            $"<o:Pages>1</o:Pages>{newLine}\t\t" +
            $"<o:Words>0</o:Words>{newLine}\t\t" +
            $"<o:Characters>0</o:Characters>{newLine}\t\t" +
            $"<o:Lines>1</o:Lines>{newLine}\t\t" +
            $"<o:Paragraphs>1</o:Paragraphs>{newLine}\t\t" +
            $"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{newLine}\t\t" +
            $"<o:Version>11.5606</o:Version>{newLine}\t" +
        "</o:DocumentProperties>"));
else
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### أنظر أيضا

* class [SaveOptions](../saveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
