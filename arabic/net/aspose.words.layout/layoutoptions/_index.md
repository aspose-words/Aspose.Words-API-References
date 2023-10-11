---
title: Class LayoutOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Layout.LayoutOptions فصل. يحمل الخيارات التي تسمح بالتحكم في عملية تخطيط المستند.
type: docs
weight: 3350
url: /ar/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

يحمل الخيارات التي تسمح بالتحكم في عملية تخطيط المستند.

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
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | يحصل على أو مجموعات[`IPageLayoutCallback`](../ipagelayoutcallback/) التنفيذ المستخدم بواسطة نموذج تخطيط الصفحة. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | الحصول على أو تعيين الطريقة التي يتم بها عرض التعليقات. القيمة الافتراضية هيShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | الحصول على أو تعيين وضع السلوك لحساب أرقام الصفحات عندما يقوم قسم مستمر بإعادة تشغيل ترقيم الصفحات. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | الحصول على أو تعيين الإشارة إلى ما إذا كان خيار التوافق "استخدام مقاييس الطابعة لتخطيط المستند" قد تم تجاهله. الإعداد الافتراضي هو`حقيقي` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | الحصول على أو تعيين إشارة إلى ما إذا كان ينبغي استخدام قياسات الخط الأصلي بعد استبدال الخط. الافتراضي هو`حقيقي` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | الحصول على خيارات المراجعة. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | الحصول على أو تعيين الإشارة إلى ما إذا كان سيتم عرض النص المخفي في المستند. الافتراضي هو`خطأ شنيع` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | الحصول على أو تعيين الإشارة إلى ما إذا كان سيتم عرض علامات الفقرة أم لا. الإعداد الافتراضي هو`خطأ شنيع` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | يحصل على أو مجموعات[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) التنفيذ المستخدم لميزات عرض الطباعة المتقدمة. |

### ملاحظات

لا يمكنك إنشاء مثيلات لهذه الفئة مباشرة. استخدم ال[`LayoutOptions`](../../aspose.words/document/layoutoptions/) الخاصية للوصول إلى خيارات التخطيط لهذا المستند.

لاحظ أنه بعد تغيير أي من الخيارات الموجودة في هذا الفصل،[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) يجب استدعاء الأسلوب حتى يتم تطبيق الخيارات التي تم تغييرها على التخطيط.

### أمثلة

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

يوضح كيفية إظهار علامات الفقرة في مستند الإخراج المعروض.

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

// أدخل مراجعة، ثم قم بتغيير لون كافة المراجعات إلى اللون الأخضر.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// قم بإزالة الشريط الذي يظهر على يسار كل سطر تمت مراجعته.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)


