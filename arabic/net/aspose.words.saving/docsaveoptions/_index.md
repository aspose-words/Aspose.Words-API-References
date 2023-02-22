---
title: Class DocSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.DocSaveOptions فصل. يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفDoc أو Dot التنسيق .
type: docs
weight: 4670
url: /ar/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

يمكن استخدامها لتحديد خيارات إضافية عند حفظ مستند في ملفDoc أو Dot التنسيق .

```csharp
public class DocSaveOptions : SaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقDoc التنسيق . |
| [DocSaveOptions](docsaveoptions/#constructor_1)(SaveFormat) | يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقDoc أو Dot التنسيق . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | الحصول على أو تعيين قيمة منطقية تشير إلى ما إذا كان سيتم السماح بدمج الخطوط مع مخططات PostScript عند حفظ خطوط TrueType في مستند ما . القيمة الافتراضية هي **خاطئة** . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | متى`خاطئة` ، لا يتم ضغط ملفات التعريف الصغيرة لسبب الأداء. القيمة الافتراضية هي **حقيقي** ، يتم ضغط كافة ملفات التعريف بغض النظر عن حجمها. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | الحصول على أو تعيين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ / الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) . القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) . |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد . |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML . |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawingML . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما يكون صحيحًا ، يتسبب في تضمين اسم ونسخة Aspose. Words في الملفات المنتجة. القيمة الافتراضية هي **حقيقي** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | الحصول على القيمة أو تعيينها لتحديد تنسيقات المستندات التي يُسمح لها بالتعيين[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . بشكل افتراضي فقطFlatOpc يُسمح بتعيين تنسيق المستند. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | الحصول على أو تعيين قيمة تحدد كيفية عرض كائنات الحبر (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** . |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | الحصول على / تعيين كلمة مرور لتشفير المستند باستخدام طريقة تشفير RC4. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | متى`حقيقي` ، جميلة تنسيقات الإخراج حيثما أمكن ذلك. القيمة الافتراضية هي **خاطئة** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم الاتصال به أثناء حفظ المستند ويقبل البيانات حول حفظ التقدم . |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا . يمكن أن يكونDoc أوDot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | متى`خاطئة` ، لا يتم حفظ بيانات PictureBullet في وثيقة الإخراج. القيمة الافتراضية هي **حقيقي** . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | متى`خاطئة` ، لا يتم حفظ بيانات RoutingSlip في مستند الإخراج **حقيقي** . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي ، هذه الخاصية هي`لا شيء` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية خاطئة ؛ |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث حقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت . القيمة الافتراضية لهذه الخاصية هي **حقيقي** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان ملف[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان محتوى[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) يتم تحديثه قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام الصقل للعرض أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

### ملاحظات

في الوقت الحالي يوفر فقط ملف[`SaveFormat`](./saveformat/) الخاصية ، ولكن في المستقبل ستتم إضافة خيارات أخرى ، مثل كلمة مرور التشفير أو إعدادات التوقيع الرقمي.

### أمثلة

يوضح كيفية تعيين خيارات الحفظ لتنسيقات Microsoft Word القديمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// تعيين كلمة مرور تحمي تحميل المستند بواسطة Microsoft Word أو Aspose.Words.
// لاحظ أن هذا لا يقوم بتشفير محتويات المستند بأي شكل من الأشكال.
options.Password = "MyPassword";

// إذا كان المستند يحتوي على قسيمة توجيه ، فيمكننا الاحتفاظ بها أثناء الحفظ عن طريق ضبط هذه العلامة على "true".
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// لتتمكن من تحميل المستند ،
// سنحتاج إلى تطبيق كلمة المرور التي حددناها في كائن DocSaveOptions في كائن LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [SaveOptions](../saveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


