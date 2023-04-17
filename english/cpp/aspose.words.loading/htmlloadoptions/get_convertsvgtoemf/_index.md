---
title: Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf method
linktitle: get_ConvertSvgToEmf
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf method. Gets or sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is false and, if possible, loaded SVG images are stored as is without conversion in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.loading/htmlloadoptions/get_convertsvgtoemf/
---
## HtmlLoadOptions::get_ConvertSvgToEmf method


Gets or sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is **false** and, if possible, loaded SVG images are stored as is without conversion.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf() const
```

## Remarks


Newer versions of MS Word support SVG images natively. If the MS Word version specified in load options supports SVG, Aspose.Words will store SVG images as is without conversion. If SVG is not supported, loaded SVG images will be converted to the EMF format.

If, however, this option is set to **true**, Aspose.Words will convert loaded SVG images to EMF even if SVG images are supported by the specified version of MS Word.

## Examples



Shows how to convert SVG objects to a different format when saving HTML documents. 
```cpp
String html =
    u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        "
    u"<text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// Use 'ConvertSvgToEmf' to turn back the legacy behavior
// where all SVG images loaded from an HTML document were converted to EMF.
// Now SVG images are loaded without conversion
// if the MS Word version specified in load options supports SVG images natively.
auto loadOptions = MakeObject<HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = MakeObject<Document>(MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// This document contains a <svg> element in the form of text.
// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation handles this object.
// Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
// Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
// Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
auto options = MakeObject<HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.MetafileFormat.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
case HtmlMetafileFormat::Png:
    ASSERT_TRUE(outDocContents.Contains(
        String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") +
        u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
        u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
    break;

case HtmlMetafileFormat::Svg:
    ASSERT_TRUE(outDocContents.Contains(
        String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") +
        u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
    break;

case HtmlMetafileFormat::EmfOrWmf:
    ASSERT_TRUE(outDocContents.Contains(
        String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") +
        u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
        u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
    break;
}
```

## See Also

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
