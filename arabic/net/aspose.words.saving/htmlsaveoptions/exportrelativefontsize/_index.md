---
title: HtmlSaveOptions.ExportRelativeFontSize
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ بتنسيق HTML أو MHTML أو EPUB . الافتراضي هوخاطئة .
type: docs
weight: 240
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ بتنسيق HTML أو MHTML أو EPUB . الافتراضي هو`خاطئة` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

### ملاحظات

في العديد من المستندات الحالية (HTML ، IDPF EPUB) يتم تحديد أحجام الخطوط بوحدات نسبية. يسمح هذا للتطبيقات بضبط حجم النص عند عرض / معالجة المستندات. على سبيل المثال ، يحتوي Microsoft Internet Explorer على قائمة فرعية "عرض-&gt; حجم النص" ، تحتوي إصدارات Adobe الرقمية على زرين: زيادة / تقليل حجم النص. _ إذا كنت تتوقع أن تعمل هذه الوظيفة ، فقم بتعيين`ExportRelativeFontSize` الملكية ل`حقيقي` .

يحتوي نموذج مستند Aspose Words ويعمل فقط مع وحدات حجم الخط المطلق. تحتاج الوحدات النسبية إلى منطق إضافي لإعادة حسابه من بعض الأحجام الأولية (القياسية). حجم الخط من **طبيعي** يتم أخذ نمط المستند كمعيار. على سبيل المثال ، إذا **طبيعي** يحتوي على خط 12 نقطة وبعض النصوص 18 نقطة ، فسيتم إخراج كـ **1.5em.** إلى HTML.

عند تمكين هذا الخيار ، ستظل عناصر المستند بخلاف النص لها أحجام مطلقة. كما قد يتم التعبير عن بعض السمات المتعلقة بالنص بشكل مطلق. على وجه الخصوص ، قد ينتج عن تباعد الأسطر المحدد بقاعدة "بالضبط" نتائج غير مرغوب فيها عند قياس النص. لذلك يجب تصميم مستندات المصدر واختبارها بشكل صحيح عند التصدير باستخدام`ExportRelativeFontSize` ضبط ل`حقيقي`.

### أمثلة

يوضح كيفية استخدام أحجام الخطوط النسبية عند الحفظ بتنسيق html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// عندما نحفظ المستند بتنسيق HTML ، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كنت تريد استخدام أحجام خطوط نسبية أو مطلقة.
// قم بتعيين علامة "ExportRelativeFontSize" على "true" للإعلان عن أحجام الخطوط
 // باستخدام وحدة قياس "em" ، وهي عامل يضاعف حجم الخط الحالي.
// قم بتعيين علامة "ExportRelativeFontSize" على "خطأ" للإعلان عن أحجام الخطوط
// باستخدام وحدة القياس "pt" ، وهي الحجم المطلق للخط بالنقاط.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


