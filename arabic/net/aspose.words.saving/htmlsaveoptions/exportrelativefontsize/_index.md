---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions ExportRelativeFontSize لتخصيص أحجام الخطوط بتنسيقات HTML أو MHTML أو EPUB. حسّن سهولة القراءة!
type: docs
weight: 230
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ في HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## ملاحظات

في العديد من المستندات الحالية (HTML، IDPF EPUB)، تُحدَّد أحجام الخطوط بوحدات نسبية. يسمح هذا لتطبيقات x000d_ بتعديل حجم النص عند عرض/معالجة المستندات. على سبيل المثال، يحتوي متصفح Microsoft Internet Explorer على قائمة فرعية "عرض -&gt; حجم النص"، ويحتوي Adobe Digital Editions على زرين: زيادة/تقليل حجم النص. إذا كنت تتوقع أن تعمل هذه الوظيفة، فقم بتعيين`ExportRelativeFontSize` الممتلكات إلى`حقيقي` .

يحتوي نموذج مستند Aspose Words على وحدات حجم الخط المطلقة ويعمل بها فقط. تحتاج الوحدات النسبية إلى إعادة حساب منطقي إضافي من حجم أولي (قياسي). حجم الخط**طبيعي** يُعتَبَر نمط المستند معيارًا. على سبيل المثال، إذا**طبيعي** يحتوي على خط 12 نقطة وبعض النصوص بحجم 18 نقطة، ثم سيتم output كما يلي**1.5م.** إلى HTML.

عند تفعيل هذا الخيار، ستظل عناصر المستند، باستثناء النص، ذات أحجام مطلقة. كما يمكن التعبير عن بعض السمات المتعلقة بالنص بشكل مطلق. على وجه الخصوص، قد يؤدي تحديد تباعد الأسطر باستخدام قاعدة "بالضبط" (x000d) إلى نتائج غير مرغوب فيها عند تغيير حجم النص. لذا، يجب تصميم مستندات المصدر واختبارها بشكل صحيح عند التصدير باستخدام`ExportRelativeFontSize` تم ضبطه على`حقيقي`.

## أمثلة

يوضح كيفية استخدام أحجام الخطوط النسبية عند الحفظ في .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// عندما نحفظ المستند في HTML، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كان سيتم استخدام أحجام الخطوط النسبية أو المطلقة.
// اضبط علامة "ExportRelativeFontSize" على "true" للإعلان عن أحجام الخطوط
 // باستخدام وحدة القياس "em"، وهو عامل يضاعف حجم الخط الحالي.
// اضبط علامة "ExportRelativeFontSize" على "false" للإعلان عن أحجام الخطوط
// باستخدام وحدة القياس "pt"، وهي الحجم المطلق للخط بالنقاط.
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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
