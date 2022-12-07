---
title: get_ExportPageMargins
second_title: Aspose.Words for C++ API Reference
description: Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is false.
type: docs
weight: 287
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use a builder to insert a shape with no wrapping.
SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_WrapType(WrapType::None);

// Negative shape position values may place the shape outside of page boundaries.
// If we export this to HTML, the shape will appear truncated.
shape->set_Left(-150);

// When saving the document to HTML, we can pass a SaveOptions object
// to decide whether to adjust the page to display out-of-bounds objects fully.
// If we set the "ExportPageMargins" flag to "true", the shape will be fully visible in the output HTML.
// If we set the "ExportPageMargins" flag to "false",
// our document will display the shape truncated as we would see it in Microsoft Word.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportPageMargins.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section1\"><p style=\"margin-top:0pt; margin-left:151pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:221.85pt; margin-bottom:0pt\">"));
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
