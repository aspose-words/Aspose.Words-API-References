---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ExportRoundtripInformation في HtmlSaveOptions للتحكم في بيانات الرحلات ذهابًا وإيابًا بتنسيقات HTML وMHTML وEPUB. حسّن صادراتك اليوم!
type: docs
weight: 240
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

يحدد ما إذا كان سيتم كتابة معلومات الرحلة ذهابًا وإيابًا عند الحفظ في HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` لـ HTML و`خطأ شنيع` لـ MHTML و EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## ملاحظات

يتيح حفظ معلومات الرحلة ذهابًا وإيابًا استعادة خصائص المستند مثل علامات التبويب وتعليقات والرؤوس والتذييلات أثناء تحميل مستندات HTML مرة أخرى في[`Document`](../../../aspose.words/document/) هدف.

متى`حقيقي`يتم تصدير معلومات الرحلة ذهابًا وإيابًا كـ -aw-* CSS properties للعناصر HTML المقابلة.

متى`خطأ شنيع`، لا يؤدي ذلك إلى إخراج معلومات الذهاب والإياب إلى الملفات المنتجة.

## أمثلة

يوضح كيفية الحفاظ على العناصر المخفية عند التحويل إلى .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عند تحويل مستند إلى .html، يتم إخفاء بعض العناصر مثل الإشارات المرجعية المخفية ومواضع الشكل الأصلية،
// أو سيتم إزالة الحواشي السفلية أو تحويلها إلى نص عادي وبالتالي سيتم فقدها فعليًا.
// سيؤدي الحفظ باستخدام كائن HtmlSaveOptions مع تعيين ExportRoundtripInformation على true إلى الحفاظ على هذه العناصر.

// عندما نحفظ المستند في HTML، يمكننا تمرير كائن SaveOptions لتحديد
// كيف ستقوم عملية الحفظ بتصدير عناصر المستند التي لا يدعمها HTML أو لا يستخدمها،
// مثل العلامات المرجعية المخفية ومواضع الشكل الأصلية.
// إذا قمنا بتعيين علم "ExportRoundtripInformation" إلى "true"، فستحافظ عملية الحفظ على هذه العناصر.
// إذا قمنا بتعيين علم "ExportRoundTripInformation" إلى "false"، فسوف تقوم عملية الحفظ بتجاهل هذه العناصر.
// سنرغب في الحفاظ على هذه العناصر إذا كنا نعتزم تحميل HTML المحفوظ باستخدام Aspose.Words،
// حيث يمكن أن تكون ذات فائدة مرة أخرى.
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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
