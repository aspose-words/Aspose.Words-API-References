---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::set_ExportEmbeddedCss method
linktitle: set_ExportEmbeddedCss
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::set_ExportEmbeddedCss method. Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/set_exportembeddedcss/
---
## HtmlFixedSaveOptions::set_ExportEmbeddedCss method


Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

```cpp
void Aspose::Words::Saving::HtmlFixedSaveOptions::set_ExportEmbeddedCss(bool value)
```

## Examples


Shows how to determine where to store CSS stylesheets when exporting a document to Html.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

// When we export a document to html, Aspose.Words will also create a CSS stylesheet to format the document with.
// Setting the "ExportEmbeddedCss" flag to "true" save the CSS stylesheet to a .css file,
// and link to the file from the html document using a <link> element.
// Setting the flag to "false" will embed the CSS stylesheet within the Html document,
// which will create only one file instead of two.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```
## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
