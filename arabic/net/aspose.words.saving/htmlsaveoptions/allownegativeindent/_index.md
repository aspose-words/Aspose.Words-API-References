---
title: HtmlSaveOptions.AllowNegativeIndent
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كانت المسافات البادئة اليمنى واليسرى السالبة للفقرات طبيعية عند الحفظ بتنسيق HTML أو MHTML أو EPUB. القيمة الافتراضية هيخاطئة .
type: docs
weight: 20
url: /ar/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

يحدد ما إذا كانت المسافات البادئة اليمنى واليسرى السالبة للفقرات طبيعية عند الحفظ بتنسيق HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خاطئة` .

```csharp
public bool AllowNegativeIndent { get; set; }
```

### ملاحظات

عند عدم السماح بالمسافة البادئة السالبة ، يتم تصديرها كهامش صفري إلى HTML. عند السماح بمسافة بادئة سالبة ، قد تظهر الفقرة جزئيًا خارج نافذة المستعرض .

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

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


