---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Layout.LayoutOptions لتحسين التحكم في تخطيط المستند، وتعزيز تجربة معالجة الكلمات لديك باستخدام خيارات التخصيص المرنة.
type: docs
weight: 3800
url: /ar/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

يحتوي على الخيارات التي تسمح بالتحكم في عملية تخطيط المستند.

لمعرفة المزيد، قم بزيارة[التحويل إلى تنسيق الصفحة الثابتة](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) مقالة توثيقية.

```csharp
public class LayoutOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | يحصل أو يعين[`IPageLayoutCallback`](../ipagelayoutcallback/) التنفيذ المستخدم بواسطة نموذج تخطيط الصفحة. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | يحصل على طريقة عرض التعليقات أو يعينها. القيمة الافتراضية هيShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | يحصل على أو يعين وضع السلوك لحساب أرقام الصفحات عندما يقوم القسم المستمر بإعادة تشغيل ترقيم الصفحات. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | يحصل على أو يعين مؤشرًا لما إذا كان سيتم تجاهل خيار التوافق "استخدام مقاييس الطابعة لتخطيط المستند". الافتراضي هو`حقيقي` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | يحصل على أو يعين مؤشرًا حول ما إذا كان يجب استخدام مقاييس الخط الأصلية بعد استبدال الخط. الافتراضي هو`حقيقي` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | يحصل على خيارات المراجعة. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | يحصل على أو يعين مؤشرًا لما إذا كان يتم عرض النص المخفي في المستند. الافتراضي هو`خطأ شنيع` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | يحصل على أو يعين مؤشرًا لما إذا كانت علامات الفقرة يتم عرضها أم لا. الافتراضي هو`خطأ شنيع` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | يحصل أو يعين[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) التنفيذ المستخدم لميزات عرض الطباعة المتقدمة. |

## ملاحظات

لا تُنشئ مثيلات لهذه الفئة مباشرةً. استخدم[`LayoutOptions`](../../aspose.words/document/layoutoptions/) الخاصية للوصول إلى خيارات التخطيط لهذه الوثيقة.

لاحظ أنه بعد تغيير أي من الخيارات الموجودة في هذه الفئة،[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) يجب استدعاء method لتطبيق الخيارات المتغيرة على التخطيط.

## أمثلة

يوضح كيفية إخفاء النص في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// أدخل نصًا مخفيًا، ثم حدد ما إذا كنا نرغب في حذفه من المستند المعروض.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

يوضح كيفية إظهار علامات الفقرات في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// أضف بعض الفقرات، ثم قم بتمكين علامات الفقرات لإظهار نهايات الفقرات
// مع رمز pilcrow (¶) عندما نقوم بعرض المستند.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

يوضح كيفية تغيير مظهر المراجعات في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج مراجعة، ثم قم بتغيير لون جميع المراجعات إلى اللون الأخضر.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// قم بإزالة الشريط الذي يظهر على يسار كل سطر تمت مراجعته.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
