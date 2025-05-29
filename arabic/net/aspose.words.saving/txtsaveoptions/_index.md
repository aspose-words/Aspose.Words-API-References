---
title: TxtSaveOptions Class
linktitle: TxtSaveOptions
articleTitle: TxtSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات حفظ Aspose.Words.TxtSave لتحسين حفظ المستندات. خصّص تنسيق نصك بخيارات فعّالة لتحقيق أفضل النتائج.
type: docs
weight: 6460
url: /ar/net/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class

يمكن استخدامه لتحديد خيارات إضافية عند حفظ مستند فيText تنسيق.

لمعرفة المزيد، قم بزيارة[تحديد خيارات الحفظ](https://docs.aspose.com/words/net/specify-save-options/) مقالة توثيقية.

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
| [AddBidiMarks](../../aspose.words.saving/txtsaveoptions/addbidimarks/) { get; set; } | يحدد ما إذا كان سيتم إضافة علامات ثنائية الاتجاه قبل كل تشغيل BiDi عند التصدير بتنسيق نص عادي. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان سيتم السماح بتضمين الخطوط مع الخطوط العريضة لـ PostScript عند تضمين خطوط TrueType في مستند عند حفظه. القيمة الافتراضية هي`خطأ شنيع` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | يحصل على أو يعين المنطقة الزمنية المحلية المخصصة المستخدمة لحقول التاريخ/الوقت. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | يحصل على المسار إلى القالب الافتراضي (بما في ذلك اسم الملف) أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض التأثيرات ثلاثية الأبعاد أو يعينها. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض تأثيرات DrawingML أو يعينها. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض أشكال DrawingML أو يعينها. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | يحدد الترميز الذي سيتم استخدامه عند التصدير بتنسيقات نصية. القيمة الافتراضية هي**ترميز UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | عندما`حقيقي` ، يؤدي إلى تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي`حقيقي` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | يحدد الطريقة التي يتم بها تصدير الرؤوس والتذييلات إلى تنسيقات النص. القيمة الافتراضية هيPrimaryOnly . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | يسمح بتحديد ما إذا كان ينبغي الحفاظ على فواصل الصفحات أثناء التصدير. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | يحصل على قيمة تحدد كيفية عرض كائنات الحبر (InkML) أو يعينها. |
| [ListIndentation](../../aspose.words.saving/txtsaveoptions/listindentation/) { get; } | يحصل على[`TxtListIndentation`](../txtlistindentation/)كائن يحدد عدد الأحرف التي سيتم استخدامها لتحديد مسافة بادئة لمستويات القائمة. بشكل افتراضي، يكون عدد الأحرف '\0' صفرًا، وهذا يعني عدم وجود مسافة بادئة. |
| [MaxCharactersPerLine](../../aspose.words.saving/txtsaveoptions/maxcharactersperline/) { get; set; } | يحصل على أو يعين قيمة عددية تحدد الحد الأقصى لعدد الأحرف في كل سطر واحد. القيمة الافتراضية هي 0، وهذا يعني عدم وجود حد. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | يحصل على القيمة أو يعينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | يحدد السلسلة التي سيتم استخدامها كفاصل للفقرة عند التصدير بتنسيقات نصية. |
| [PreserveTableLayout](../../aspose.words.saving/txtsaveoptions/preservetablelayout/) { get; set; } | يحدد ما إذا كان ينبغي للبرنامج محاولة الحفاظ على تخطيط الجداول عند الحفظ بتنسيق نص عادي. القيمة الافتراضية هي`خطأ شنيع` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | عندما`حقيقي` ، تنسيقات الإخراج الجميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | يتم استدعاؤها أثناء حفظ المستند وتقبل البيانات حول تقدم الحفظ. |
| override [SaveFormat](../../aspose.words.saving/txtsaveoptions/saveformat/) { get; set; } | يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاText . |
| [SimplifyListLabels](../../aspose.words.saving/txtsaveoptions/simplifylistlabels/) { get; set; } | يحدد ما إذا كان يجب على البرنامج تبسيط تسميات القائمة في حالة عدم تمثيل تنسيق التسمية المعقدة بشكل كافٍ بواسطة نص عادي. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | يحدد المجلد للملفات المؤقتة المستخدمة عند الحفظ في ملف DOC أو DOCX. بشكل افتراضي، تكون هذه الخاصية`باطل` ولا يتم استخدام أي ملفات مؤقتة. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | يحدد ما إذا كانت سمات الخط ستتغير وفقًا لرمز الحرف المستخدم. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب تحديث حقول أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام التنعيم للرسم أم لا. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام خوارزميات عرض عالية الجودة (أي بطيئة) أم لا. |

## أمثلة

يوضح كيفية حفظ مستند .txt باستخدام فاصل فقرة مخصص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// تعيين "ParagraphBreak" إلى قيمة مخصصة نرغب في وضعها في نهاية كل فقرة.
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
