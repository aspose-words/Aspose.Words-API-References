---
title: Enum HtmlElementSizeOutputMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.HtmlElementSizeOutputMode تعداد. يحدد كيفية تصدير Aspose.Words عروض وارتفاعات العناصر إلى HTML و MHTML و EPUB.
type: docs
weight: 4800
url: /ar/net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

يحدد كيفية تصدير Aspose.Words عروض وارتفاعات العناصر إلى HTML و MHTML و EPUB.

```csharp
public enum HtmlElementSizeOutputMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| All | `0` | يتم تصدير جميع أحجام العناصر ، سواء في الوحدات المطلقة أو النسبية المحددة في المستند. |
| RelativeOnly | `1` | يتم تصدير أحجام العناصر فقط إذا كانت محددة بوحدات نسبية في المستند. لا يتم تصدير الأحجام الثابتة في هذا الوضع. سيحسب الوكلاء المرئيون الأحجام المفقودة لجعل تخطيط المستند أكثر طبيعية . |
| None | `2` | لا يتم تصدير أحجام العناصر. سيقوم الوكلاء المرئيون ببناء التخطيط تلقائيًا وفقًا للعلاقة بين العناصر. |

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

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


