---
title: Class TxtSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.TxtSaveOptions فصل. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفText التنسيق .
type: docs
weight: 5380
url: /ar/net/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفText التنسيق .

```csharp
public class TxtSaveOptions : TxtSaveOptionsBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TxtSaveOptions](txtsaveoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AddBidiMarks](../../aspose.words.saving/txtsaveoptions/addbidimarks/) { get; set; } | يحدد ما إذا كان سيتم إضافة علامات ثنائية الاتجاه قبل كل تشغيل ثنائي الاتجاه عند التصدير بتنسيق نص عادي. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) . القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) . |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد . |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | يحدد الترميز الذي سيتم استخدامه عند التصدير بتنسيقات نصية. القيمة الافتراضية هي **الترميز** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | يحدد طريقة تصدير الرؤوس والتذييلات إلى تنسيقات النص. القيمة الافتراضية هيPrimaryOnly . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | يسمح بتحديد ما إذا كان يجب الاحتفاظ بفواصل الصفحات أثناء التصدير. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [ListIndentation](../../aspose.words.saving/txtsaveoptions/listindentation/) { get; } | الحصول على كائن ListIndentation الذي يحدد عدد الأحرف التي يجب استخدامها والمسافة البادئة لمستويات القائمة. |
| [MaxCharactersPerLine](../../aspose.words.saving/txtsaveoptions/maxcharactersperline/) { get; set; } | الحصول على أو تعيين قيمة عدد صحيح تحدد الحد الأقصى لعدد الأحرف في كل سطر. القيمة الافتراضية هي 0 ، وهذا يعني عدم وجود حد. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | يحدد السلسلة التي سيتم استخدامها كفاصل فقرة عند التصدير بتنسيقات نصية. |
| [PreserveTableLayout](../../aspose.words.saving/txtsaveoptions/preservetablelayout/) { get; set; } | يحدد ما إذا كان يجب على البرنامج محاولة الحفاظ على تخطيط الجداول عند الحفظ بتنسيق نص عادي. القيمة الافتراضية هي **خاطئة** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم . |
| override [SaveFormat](../../aspose.words.saving/txtsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ . يمكن فقط أن يكونText . |
| [SimplifyListLabels](../../aspose.words.saving/txtsaveoptions/simplifylistlabels/) { get; set; } | يحدد ما إذا كان يجب على البرنامج تبسيط تسميات القائمة في حالة تنسيق الملصق المعقد الذي لا يتم تمثيله بشكل كافٍ بنص عادي. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت . القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

### أمثلة

يوضح كيفية حفظ مستند .txt مع فاصل فقرة مخصص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// قم بإنشاء كائن "TxtSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند على نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// اضبط "ParagraphBreak" على قيمة مخصصة نرغب في وضعها في نهاية كل فقرة.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### أنظر أيضا

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


