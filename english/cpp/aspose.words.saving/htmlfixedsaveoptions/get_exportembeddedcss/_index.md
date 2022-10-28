---
title: get_ExportEmbeddedCss
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.
type: docs
weight: 40
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions.get_ExportEmbeddedCss method


Specifies whether the CSS (Cascading [Style](../../../aspose.words/style/) Sheet) should be embedded into Html document.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Examples




Shows how to determine where to store CSS stylesheets when exporting a document to Html. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// When we export a document to html, Aspose.Words will also create a CSS stylesheet to format the document with.
// Setting the "ExportEmbeddedCss" flag to "true" save the CSS stylesheet to a .css file,
// and link to the file from the html document using a <link> element.
// Setting the flag to "false" will embed the CSS stylesheet within the Html document,
// which will create only one file instead of two.
auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents,
                    u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")
                    ->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(ArtifactsDir + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

