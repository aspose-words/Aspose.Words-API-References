---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts method
linktitle: get_ExportEmbeddedFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts method. Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Examples



Shows how to determine where to store embedded fonts when exporting a document to Html. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Embedded font.docx");

// When we export a document with embedded fonts to .html,
// Aspose.Words can place the fonts in two possible locations.
// Setting the "ExportEmbeddedFonts" flag to "true" will store the raw data for embedded fonts within the CSS stylesheet,
// in the "url" property of the "@font-face" rule. This may create a huge CSS stylesheet file
// and reduce the number of external files that this HTML conversion will create.
// Setting this flag to "false" will create a file for each font.
// The CSS stylesheet will link to each font file using the "url" property of the "@font-face" rule.
auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents,
                    u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")
                    ->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")
                     ->LINQ_Count([](String f) { return f.EndsWith(u".woff"); }));
}
else
{
    ASSERT_TRUE(
        System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; "
                                                                       u"src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")
            ->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")
                     ->LINQ_Count([](String f) { return f.EndsWith(u".woff"); }));
}
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
