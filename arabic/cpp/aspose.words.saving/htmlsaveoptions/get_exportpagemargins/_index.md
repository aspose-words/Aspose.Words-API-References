---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins طريقة"
linktitle: "get_ExportPageMargins"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins طريقة. تحدد ما إذا كانت هوامش الصفحة تُصدَّر إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي false في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


يحدد ما إذا كانت هوامش الصفحة تُصدر إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## أمثلة



يظهر كيفية عرض الكائنات خارج الحدود في مستندات HTML الناتجة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم مُنشئًا لإدراج شكل بدون تغليف.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// قد تؤدي قيم موضع الشكل السلبية إلى وضع الشكل خارج حدود الصفحة.
// إذا صدّرنا هذا إلى HTML، سيظهر الشكل مقطوعًا.
shape->set_Left(-150);

// عند حفظ المستند كـ HTML، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كان يجب تعديل الصفحة لعرض الكائنات خارج الحدود بالكامل.
// إذا ضبطنا علم "ExportPageMargins" على "true", سيكون الشكل مرئيًا بالكامل في HTML الناتج.
// إذا ضبطنا علم "ExportPageMargins" على "false",
// ستعرض مستندنا الشكل مقطوعًا كما نراه في Microsoft Word.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
