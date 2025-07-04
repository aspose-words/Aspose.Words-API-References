---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages method
linktitle: get_ExportEmbeddedImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages method. Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Examples



Shows how to determine where to store images when exporting a document to Html. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// When we export a document with embedded images to .html,
// Aspose.Words can place the images in two possible locations.
// Setting the "ExportEmbeddedImages" flag to "true" will store the raw data
// for all images within the output HTML document, in the "src" attribute of <image> tags.
// Setting this flag to "false" will create an image file in the local file system for every image,
// and store all these files in a separate folder.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
