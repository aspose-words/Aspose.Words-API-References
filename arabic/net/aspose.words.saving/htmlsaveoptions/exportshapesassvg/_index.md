---
title: HtmlSaveOptions.ExportShapesAsSvg
linktitle: ExportShapesAsSvg
articleTitle: ExportShapesAsSvg
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام HtmlSaveOptions ExportShapesAsSvg لتحويل عقد الشكل إلى صور SVG عند الحفظ بتنسيقات HTML أو MHTML أو EPUB أو AZW3.
type: docs
weight: 250
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

يتحكم فيما إذا كان[`Shape`](../../../aspose.words.drawing/shape/)يتم تحويل العقد إلى صور SVG عند حفظ x000d_ إلى HTML أو MHTML أو EPUB أو AZW3. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

## ملاحظات

إذا تم تعيين هذا الخيار على`حقيقي` ،[`Shape`](../../../aspose.words.drawing/shape/) يتم تصدير العقد كعناصر &lt;svg&gt;. وإلا، يتم تقديمها إلى خرائط بتات ويتم تصديرها كعناصر &lt;img&gt;.

## أمثلة

يوضح كيفية تصدير الشكل كرسومات متجهية قابلة للتطوير.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// عندما نحفظ المستند في HTML، يمكننا تمرير كائن SaveOptions
// لتحديد كيفية قيام عملية الحفظ بتصدير أشكال مربع النص.
// إذا قمنا بتعيين علامة "ExportTextBoxAsSvg" إلى "true"،
// ستعمل عملية الحفظ على تحويل الأشكال التي تحتوي على نص إلى كائنات SVG.
// إذا قمنا بتعيين علامة "ExportTextBoxAsSvg" إلى "false"،
// ستعمل عملية الحفظ على تحويل الأشكال التي تحتوي على نص إلى صور.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
