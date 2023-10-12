---
title: HtmlSaveOptions.ExportRoundtripInformation
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كان سيتم كتابة معلومات رحلة الذهاب والإياب عند الحفظ في HTML أو MHTML أو EPUB. القيمة الافتراضية هيحقيقي لـ HTML وخطأ شنيع لـ MHTML وEPUB.
type: docs
weight: 240
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

يحدد ما إذا كان سيتم كتابة معلومات رحلة الذهاب والإياب عند الحفظ في HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` لـ HTML و`خطأ شنيع` لـ MHTML وEPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### ملاحظات

يتيح حفظ معلومات رحلة الذهاب والعودة استعادة خصائص المستند مثل علامات الجدولة وتعليقات والرؤوس والتذييلات أثناء تحميل مستندات HTML مرة أخرى إلى ملف[`Document`](../../../aspose.words/document/) هدف.

متى`حقيقي`، يتم تصدير معلومات رحلة الذهاب والإياب كـ -aw-* CSS property لعناصر HTML المقابلة.

متى`خطأ شنيع`، لا يؤدي إلى إخراج أي معلومات ذهابًا وإيابًا في الملفات المنتجة.

### أمثلة

يوضح كيفية الحفاظ على العناصر المخفية عند التحويل إلى .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عند تحويل مستند إلى .html، تظهر بعض العناصر مثل الإشارات المرجعية المخفية، ومواضع الأشكال الأصلية،
// أو ستتم إزالة الحواشي السفلية أو تحويلها إلى نص عادي وسيتم فقدها فعليًا.
// الحفظ باستخدام كائن HtmlSaveOptions مع تعيين ExportRoundtripInformation على القيمة true سوف يحافظ على هذه العناصر.

// عندما نحفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions لتحديده
// كيف ستقوم عملية الحفظ بتصدير عناصر المستند التي لا يدعمها HTML أو يستخدمها،
// مثل الإشارات المرجعية المخفية ومواضع الأشكال الأصلية.
// إذا قمنا بتعيين علامة "ExportRoundtripInformation" على "صحيح"، فستحافظ عملية الحفظ على هذه العناصر.
// إذا قمنا بتعيين علامة "ExportRoundTripInformation" على "خطأ"، فستتجاهل عملية الحفظ هذه العناصر.
// سنرغب في الحفاظ على هذه العناصر إذا أردنا تحميل HTML المحفوظ باستخدام Aspose.Words،
// لأنها يمكن أن تكون ذات فائدة مرة أخرى.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


