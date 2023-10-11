---
title: HtmlSaveOptions.ExportRelativeFontSize
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ في HTML أو MHTML أو EPUB. الإعداد الافتراضي هوخطأ شنيع .
type: docs
weight: 230
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ في HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

### ملاحظات

في العديد من المستندات الموجودة (HTML، IDPF EPUB) يتم تحديد أحجام الخطوط بوحدات نسبية. يتيح ذلك لتطبيقات ضبط حجم النص عند عرض/معالجة المستندات. على سبيل المثال، يحتوي Microsoft Internet Explorer على القائمة الفرعية "عرض-&gt;حجم النص"، ويحتوي Adobe Digital Editions على زرين: زيادة/تقليل حجم النص. إذا كنت تتوقع أن تعمل هذه الوظيفة، فقم بتعيين`ExportRelativeFontSize` الملكية ل`حقيقي` .

يحتوي نموذج مستند Aspose Words على وحدات حجم الخط المطلقة ويعمل بها فقط. تحتاج الوحدات النسبية إلى منطق إضافي لإعادة حسابه من بعض الحجم الأولي (القياسي). حجم الخط **طبيعي** يتم أخذ نمط المستند بشكل قياسي. على سبيل المثال، إذا **طبيعي** يحتوي على خط بحجم 12pt وبعض النصوص بحجم 18pt، ثم سيتم إخراجه كـ **1.5 م.** إلى HTML.

عند تمكين هذا الخيار، ستظل عناصر المستند بخلاف النص ذات أحجام مطلقة. كما قد يتم التعبير عن بعض السمات المتعلقة بالنص بشكل مطلق. على وجه الخصوص، قد يؤدي تباعد الأسطر المحدد بقاعدة "بالضبط" إلى نتائج غير مرغوب فيها عند تغيير حجم النص. لذلك يجب تصميم المستندات المصدر واختبارها بشكل صحيح عند التصدير باستخدام`ExportRelativeFontSize` ضبط ل`حقيقي`.

### أمثلة

يوضح كيفية استخدام أحجام الخطوط النسبية عند الحفظ بتنسيق .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// عندما نحفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كنت تريد استخدام أحجام الخطوط النسبية أو المطلقة.
// قم بتعيين علامة "ExportRelativeFontSize" على "true" للإعلان عن أحجام الخطوط
 // باستخدام وحدة القياس "em"، وهو عامل يضاعف حجم الخط الحالي.
// اضبط علامة "ExportRelativeFontSize" على "خطأ" للإعلان عن أحجام الخطوط
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
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


