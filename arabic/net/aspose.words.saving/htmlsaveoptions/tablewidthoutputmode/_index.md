---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words لـ .NET
description: حسّن تصديرات HTML باستخدام وضع عرض وإخراج جدول HtmlSaveOptions. تحكّم بعرض الصفوف والخلايا في الجدول لتنسيق MHTML وEPUB بسلاسة.
type: docs
weight: 480
url: /ar/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

يتحكم في كيفية تصدير عرض الجدول والصف والخليّة إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## ملاحظات

بتنسيق HTML، عناصر الجدول والصف والخليّة (**&lt;الجدول&gt;** ،**&lt;تر&gt;** ،**&lt;ث&gt;** ،**&lt;تد&gt;**)يمكن تحديد عرض إما كنسبة مئوية أو كوحدات مطلقة. في مستند في Aspose.Words، يمكن تحديد عرض الجداول والصفوف والخلايا باستخدام وحدات نسبية أو مطلقة أيضًا.

عند تحويل مستند إلى HTML باستخدام Aspose.Words، قد ترغب في التحكم في كيفية تصدير عرض الجدول والصفوف والخلايا للتأثير على كيفية عرض المستند الناتج في الوكيل المرئي (على سبيل المثال، المتصفح أو العارض).

استخدم هذه الخاصية كمرشح لتحديد قيم عرض الجدول المُصدَّرة إلى المستند الوجهة. على سبيل المثال، إذا كنت تُحوِّل مستندًا إلى EPUB وتنوي عرضه على جهاز قراءة محمول، فربما ترغب في تجنب تصدير قيم العرض المطلقة. للقيام بذلك، عليك تحديد وضع الإخراج.RelativeOnly أوNone حتى يتمكن المشاهد على الجهاز المحمول من تخطيط الجدول بحيث يتناسب مع عرض الشاشة بأفضل ما يمكن.

## أمثلة

يوضح كيفية الحفاظ على المسافات البادئة السلبية في ملف .html الناتج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج جدول بمسافة بادئة سلبية، مما سيؤدي إلى دفعه إلى اليسار بعد حدود الصفحة اليسرى.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// قم بإدراج جدول بمسافة بادئة موجبة، مما سيؤدي إلى دفع الجدول إلى اليمين.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// عندما نحفظ مستندًا بتنسيق HTML، سيحافظ Aspose.Words فقط على المسافات البادئة السلبية
// مثل الذي طبقناه على الجدول الأول إذا قمنا بتعيين العلم "AllowNegativeIndent"
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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
