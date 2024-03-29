---
title: HtmlElementSizeOutputMode Enum
linktitle: HtmlElementSizeOutputMode
articleTitle: HtmlElementSizeOutputMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.HtmlElementSizeOutputMode تعداد. يحدد كيفية تصدير Aspose.Words لعروض العناصر وارتفاعاتها إلى HTML وMHTML وEPUB في C#.
type: docs
weight: 5060
url: /ar/net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

يحدد كيفية تصدير Aspose.Words لعروض العناصر وارتفاعاتها إلى HTML وMHTML وEPUB.

```csharp
public enum HtmlElementSizeOutputMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| All | `0` | يتم تصدير جميع أحجام العناصر، سواء بالوحدات المطلقة أو النسبية، المحددة في المستند. |
| RelativeOnly | `1` | لا يتم تصدير أحجام العناصر إلا إذا تم تحديدها بوحدات نسبية في المستند. لا يتم تصدير الأحجام الثابتة في هذا الوضع. سيقوم الوكلاء المرئيون بحساب الأحجام المفقودة لجعل تخطيط المستند أكثر طبيعية. |
| None | `2` | لا يتم تصدير أحجام العناصر. سيقوم الوكلاء المرئيون ببناء التخطيط تلقائيًا وفقًا للعلاقة بين العناصر. |

## أمثلة

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

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
