---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize"
linktitle: "get_ExportRelativeFontSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize. تحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي false في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


يحدد ما إذا كان يجب إخراج أحجام الخطوط بوحدات نسبية عند الحفظ إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## ملاحظات


في العديد من المستندات الحالية (HTML، IDPF EPUB) يتم تحديد أحجام الخطوط بوحدات نسبية. يتيح ذلك للتطبيقات تعديل حجم النص عند عرض/معالجة المستندات. على سبيل المثال، يحتوي Microsoft Internet Explorer على القائمة الفرعية "View->Text Size"، وتحتوي Adobe Digital Editions على زرين: Increase/Decrease Text Size. إذا كنت تتوقع أن تعمل هذه الوظيفة، فقم بتعيين خاصية [ExportRelativeFontSize](./) إلى **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

عند تمكين هذا الخيار، ستظل عناصر المستند غير النصية ذات أحجام مطلقة. كما قد تُعبّر بعض السمات المتعلقة بالنص بصورة مطلقة. على وجه الخصوص، قد ينتج عن تباعد الأسطر المحدد بقاعدة "exactly" نتائج غير مرغوبة عند تكبير النص. لذا يجب تصميم المستندات المصدرية واختبارها بشكل صحيح عند التصدير مع تعيين [ExportRelativeFontSize](./) إلى **true**.

## أمثلة



يعرض كيفية استخدام أحجام الخطوط النسبية عند الحفظ إلى .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كان سيتم استخدام أحجام خطوط نسبية أو مطلقة.
// قم بتعيين العلامة "ExportRelativeFontSize" إلى "true" لتحديد أحجام الخطوط
// باستخدام وحدة القياس "em"، وهي عامل يضاعف حجم الخط الحالي.
// قم بتعيين العلامة "ExportRelativeFontSize" إلى "false" لتحديد أحجام الخطوط
// باستخدام وحدة القياس "pt"، وهي الحجم المطلق للخط بالنقاط.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
