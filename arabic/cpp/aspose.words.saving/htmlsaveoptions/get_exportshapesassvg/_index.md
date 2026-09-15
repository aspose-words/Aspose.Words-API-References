---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg طريقة"
linktitle: "get_ExportShapesAsSvg"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg طريقة. يتحكم فيما إذا كانت عقد Shape تتحول إلى صور SVG عند الحفظ إلى HTML أو MHTML أو EPUB أو AZW3. القيمة الافتراضية هي false في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


يتحكم فيما إذا كانت عقد [Shape](../../../aspose.words.drawing/shape/) تتحول إلى صور SVG عند الحفظ إلى HTML أو MHTML أو EPUB أو AZW3. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## ملاحظات


إذا تم تعيين هذا الخيار إلى **true**، يتم تصدير عقد [Shape](../../../aspose.words.drawing/shape/) كعناصر <svg>. وإلا، يتم تحويلها إلى صور نقطية وتُصدّر كعناصر <img>.

## أمثلة



يظهر كيفية تصدير الشكل كرسومات متجهة قابلة للتوسيع.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
// لتحديد كيفية تصدير عملية الحفظ لأشكال مربعات النص.
// إذا قمنا بتعيين العلامة "ExportTextBoxAsSvg" إلى "true",
// ستقوم عملية الحفظ بتحويل الأشكال التي تحتوي على نص إلى كائنات SVG.
// إذا قمنا بتعيين العلامة "ExportTextBoxAsSvg" إلى "false",
// ستقوم عملية الحفظ بتحويل الأشكال التي تحتوي على نص إلى صور.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportShapesAsSvg(exportShapesAsSvg);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
