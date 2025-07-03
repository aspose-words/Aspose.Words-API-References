---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins method
linktitle: get_ExportPageMargins
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins method. Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is false in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Examples



Shows how to show out-of-bounds objects in output HTML documents. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Use a builder to insert a shape with no wrapping.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Negative shape position values may place the shape outside of page boundaries.
// If we export this to HTML, the shape will appear truncated.
shape->set_Left(-150);

// When saving the document to HTML, we can pass a SaveOptions object
// to decide whether to adjust the page to display out-of-bounds objects fully.
// If we set the "ExportPageMargins" flag to "true", the shape will be fully visible in the output HTML.
// If we set the "ExportPageMargins" flag to "false",
// our document will display the shape truncated as we would see it in Microsoft Word.
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

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
