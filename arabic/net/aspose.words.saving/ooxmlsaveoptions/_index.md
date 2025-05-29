---
title: OoxmlSaveOptions Class
linktitle: OoxmlSaveOptions
articleTitle: OoxmlSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.OoxmlSaveOptions لتحسين حفظ المستندات بتنسيقات Docx وDocm وDotx وDotm وFlatOpc باستخدام ميزات قابلة للتخصيص.
type: docs
weight: 6130
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/
---
## OoxmlSaveOptions class

يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند فيDocx ، Docm ،Dotx ،Dotm أو FlatOpc تنسيق.

لمعرفة المزيد، قم بزيارة[تحديد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

```csharp
public class OoxmlSaveOptions : SaveOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor)() | يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند فيDocx تنسيق. |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند فيDocx ، Docm ،Dotx ،Dotm أو FlatOpc تنسيق. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم السماح بتضمين الخطوط مع الخطوط العريضة لـ PostScript عند تضمين خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي`خطأ شنيع` . |
| [Compliance](../../aspose.words.saving/ooxmlsaveoptions/compliance/) { get; set; } | يحدد إصدار OOXML للمستند الناتج. القيمة الافتراضية هيEcma376_2006 . |
| [CompressionLevel](../../aspose.words.saving/ooxmlsaveoptions/compressionlevel/) { get; set; } | يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هيNormal . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | يحصل على أو يعين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | يحصل على المسار إلى القالب الافتراضي (بما في ذلك اسم الملف) أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/) { get; set; } | يحصل أو يعين[`DigitalSignatureDetails`](../digitalsignaturedetails/) الكائن المستخدم لتوقيع مستند. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد أو يعينها. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض تأثيرات DrawingML أو يعينها. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض أشكال DrawingML أو يعينها. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض كائنات الحبر (InkML) أو يعينها. |
| [KeepLegacyControlChars](../../aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/) { get; set; } | يحتفظ بالتمثيل الأصلي لأحرف التحكم القديمة. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | يحصل على القيمة أو يعينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [Password](../../aspose.words.saving/ooxmlsaveoptions/password/) { get; set; } | يحصل على/يحدد كلمة مرور لتشفير المستند باستخدام خوارزمية التشفير القياسية ECMA376. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | عندما`حقيقي` ، تنسيقات الإخراج الجميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء حفظ المستند وتقبل البيانات حول تقدم الحفظ. |
| override [SaveFormat](../../aspose.words.saving/ooxmlsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكونDocx ،Docm ، Dotx ،Dotm أوFlatOpc . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب تحديث حقول أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام التنعيم للرسم أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |
| [Zip64Mode](../../aspose.words.saving/ooxmlsaveoptions/zip64mode/) { get; set; } | يحدد ما إذا كان سيتم استخدام امتدادات تنسيق ZIP64 للمستند الناتج أم لا. القيمة الافتراضية هيNever . |

## أمثلة

يوضح كيفية تعيين مواصفات توافق OOXML للمستند المحفوظ للالتزام بها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتكوين خيارات التوافق لتتوافق مع Microsoft Word 2003،
// إدراج صورة سيؤدي إلى تحديد شكلها باستخدام VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// لا يدعم معيار OOXML "ISO/IEC 29500:2008" أشكال VML.
// إذا قمنا بتعيين خاصية "التوافق" لكائن SaveOptions إلى "OoxmlCompliance.Iso29500_2008_Strict"،
 // أي مستند نقوم بحفظه أثناء تمرير هذا الكائن يجب أن يتبع هذا المعيار.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// تحدد مستندنا المحفوظ الشكل باستخدام DML للالتزام بمعيار OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### أنظر أيضا

* class [SaveOptions](../saveoptions/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
