---
title: TableWidthOutputMode
second_title: Aspose.Words لمراجع .NET API
description: يتحكم في كيفية تصدير عرض الجدول والصف والخلية إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAll .
type: docs
weight: 460
url: /ar/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

يتحكم في كيفية تصدير عرض الجدول والصف والخلية إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### ملاحظات

في تنسيق HTML وعناصر الجدول والصف والخلية ( **&lt;جدول&gt;** و **&lt;tr&gt;** و **&lt;th&gt;** و **&lt;td&gt;**) يمكن تحديد عروضها إما بالنسبية (النسبة المئوية) أو بالوحدات المطلقة. _ x000d_ في مستند في Aspose. يمكن تحديد عرض الكلمات والجداول والصفوف والخلايا باستخدام وحدات نسبية أو مطلقة أيضًا.

عندما تقوم بتحويل مستند إلى HTML باستخدام Aspose.Words ، فقد ترغب في التحكم في كيفية تصدير عرض الجدول والصف والخلية للتأثير على كيفية عرض المستند الناتج في الوكيل المرئي (مثل المتصفح أو العارض).

استخدم هذه الخاصية كعامل تصفية لتحديد قيم عرض الجدول التي يتم تصديرها إلى المستند الوجهة ._ x000d_ على سبيل المثال ، إذا كنت تقوم بتحويل مستند إلى EPUB وتنوي عرض المستند على جهاز قراءة محمول ، فربما تريد تجنب ذلك تصدير قيم العرض المطلقة. للقيام بذلك ، تحتاج إلى تحديد وضع الإخراجRelativeOnly أوNone حتى يتمكن المشاهد على الجهاز المحمول من تخطيط الجدول ليلائم عرض الشاشة بأفضل شكل ممكن.

### أمثلة

يوضح كيفية الاحتفاظ بالمسافات البادئة السالبة في ملف .html الناتج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جدول بمسافة بادئة سالبة ، مما سيدفعه إلى اليسار بعد حد الصفحة اليسرى.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// أدخل جدولًا بمسافة بادئة موجبة ، مما سيدفع الجدول إلى اليمين.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// عندما نحفظ مستندًا بتنسيق HTML ، سيحتفظ Aspose.Words فقط بمسافات بادئة سالبة
// مثل الذي طبقناه على الجدول الأول إذا قمنا بتعيين علامة "AllowNegativeIndent"
// في كائن SaveOptions الذي سنمرره إلى "true".
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### أنظر أيضا

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode)
* class [HtmlSaveOptions](../../htmlsaveoptions)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->