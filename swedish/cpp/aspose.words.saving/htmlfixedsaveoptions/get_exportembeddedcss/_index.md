---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss metod"
linktitle: "get_ExportEmbeddedCss"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss‑metod. Anger om CSS (Cascading Style Sheet) ska bäddas in i Html-dokumentet i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


Anger om CSS (Cascading [Style](../../../aspose.words/style/) Sheet) ska bäddas in i Html-dokumentet.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Exempel



Visar hur man bestämmer var CSS‑stilmallar ska lagras när ett dokument exporteras till Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// När vi exporterar ett dokument till html skapar Aspose.Words också en CSS‑stilmall för att formatera dokumentet.
// Genom att sätta flaggan "ExportEmbeddedCss" till "true" sparas CSS‑stilmallen i en .css‑fil,
// och länkas till filen från html‑dokumentet med ett <link>-element.
// Om flaggan sätts till "false" kommer CSS‑stilmallen att bäddas in i Html‑dokumentet,
// vilket skapar endast en fil istället för två.
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

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
