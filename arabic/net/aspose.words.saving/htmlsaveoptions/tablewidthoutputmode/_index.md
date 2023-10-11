---
title: HtmlSaveOptions.TableWidthOutputMode
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يتحكم في كيفية تصدير عروض الجدول والصف والخلية إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAll .
type: docs
weight: 460
url: /ar/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

يتحكم في كيفية تصدير عروض الجدول والصف والخلية إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### ملاحظات

في تنسيق HTML، عناصر الجدول والصفوف والخلية ( **&lt;الجدول&gt;** , **&lt;تر&gt;** , **&lt;ال&gt;** , **&lt;TD&gt;**) يمكن تحديد عرضها إما بنسب نسبية (نسبة مئوية) أو بوحدات مطلقة. في مستند في Aspose.Words، يمكن تحديد عرض الجداول والصفوف والخلايا بـ باستخدام الوحدات النسبية أو المطلقة أيضًا.

عندما تقوم بتحويل مستند إلى HTML باستخدام Aspose.Words، قد ترغب في التحكم في كيفية تصدير عرض الجدول والصف والخلية للتأثير على كيفية عرض المستند الناتج في الوكيل المرئي (على سبيل المثال، المتصفح أو العارض).

استخدم هذه الخاصية كمرشح لتحديد قيم عروض الجدول التي سيتم تصديرها إلى المستند الوجهة. على سبيل المثال، إذا كنت تقوم بتحويل مستند إلى EPUB وتنوي عرض المستند على جهاز قراءة محمول، فمن المحتمل أنك تريد تجنبه تصدير قيم العرض المطلقة. للقيام بذلك تحتاج إلى تحديد وضع الإخراجRelativeOnly أوNone حتى يتمكن المشاهد على الجهاز المحمول من تخطيط الجدول ليناسب عرض الشاشة بأفضل ما يمكنه.

### أمثلة

يوضح كيفية الحفاظ على المسافات البادئة السلبية في ملف .html للإخراج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج جدول بمسافة بادئة سالبة، مما سيدفعه إلى اليسار بعد حدود الصفحة اليسرى.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// أدخل جدولًا بمسافة بادئة موجبة، مما سيدفع الجدول إلى اليمين.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// عندما نحفظ مستندًا بتنسيق HTML، سيحتفظ Aspose.Words فقط بالمسافات البادئة السلبية
// مثل الذي طبقناه على الجدول الأول إذا قمنا بتعيين علامة "AllowNegativeIndent".
// في كائن SaveOptions الذي سنمرره إلى "صحيح".
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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


