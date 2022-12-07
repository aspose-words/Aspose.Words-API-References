---
title: get_ExportEmbeddedSvg
second_title: Aspose.Words for C++ API Reference
description: Specifies whether SVG resources should be embedded into Html document. Default value is true.
type: docs
weight: 92
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


Specifies whether SVG resources should be embedded into Html document. Default value is **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## Examples



Shows how to determine where to store SVG objects when exporting a document to Html. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// When we export a document with SVG objects to .html,
// Aspose.Words can place these objects in two possible locations.
// Setting the "ExportEmbeddedSvg" flag to "true" will embed all SVG object raw data
// within the output HTML, inside <image> tags.
// Setting this flag to "false" will create a file in the local file system for each SVG object.
// The HTML will link to each file using the "data" attribute of an <object> tag.
auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedSvg(exportSvgs);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    ASSERT_FALSE(System::IO::File::Exists(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<image id=\"image004\" xlink:href=.+/>")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, u"<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>")
                    ->get_Success());
}
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
