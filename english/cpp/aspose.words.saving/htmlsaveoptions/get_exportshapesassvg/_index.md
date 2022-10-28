---
title: get_ExportShapesAsSvg
second_title: Aspose.Words for C++ API Reference
description: Controls whether Shape nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is false.
type: docs
weight: 326
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions.get_ExportShapesAsSvg method


Controls whether [Shape](../../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```


If this option is set to **true**, [Shape](../../../aspose.words.drawing/shape/) nodes are exported as <svg> elements. Otherwise, they are rendered to bitmaps and are exported as <img> elements.

## Examples




Shows how to export text boxes as scalable vector graphics. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> textBox = builder->InsertShape(ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation will export text box shapes.
// If we set the "ExportShapesAsSvg" flag to "true",
// the save operation will convert shapes with text into SVG objects.
// If we set the "ExportShapesAsSvg" flag to "false",
// the save operation will convert shapes with text into images.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportShapesAsSvg(exportShapesAsSvg);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportTextBox.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    ASSERT_TRUE(outDocContents.Contains(
        String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") +
        u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(
        String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") +
        u"<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
        u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
}
```

