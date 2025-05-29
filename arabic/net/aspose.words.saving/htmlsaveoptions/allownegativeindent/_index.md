---
title: HtmlSaveOptions.AllowNegativeIndent
linktitle: AllowNegativeIndent
articleTitle: AllowNegativeIndent
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions AllowNegativeIndent للتحكم في مسافات الفقرات عند الحفظ بتنسيق HTML أو MHTML أو EPUB. حسّن تنسيق مستندك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

يُحدد ما إذا كانت المسافات البادئة السالبة للفقرات، سواءً اليسرى أو اليمنى، طبيعية عند الحفظ بتنسيق HTML أو MHTML أو EPUB. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool AllowNegativeIndent { get; set; }
```

## ملاحظات

عندما لا يُسمح بالمسافة البادئة السلبية، يتم تصديرها بهامش صفر إلى HTML. عندما يُسمح بالمسافة البادئة السلبية، قد تظهر الفقرة جزئيًا خارج نافذة المتصفح .

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

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
