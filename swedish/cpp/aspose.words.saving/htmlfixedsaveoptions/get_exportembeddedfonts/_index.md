---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts metod"
linktitle: "get_ExportEmbeddedFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts metod. Anger om teckensnitt ska bäddas in i Html-dokumentet i Base64-format. Observera att inställning av denna flagga kan avsevärt öka storleken på den genererade Html-filen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Anger om teckensnitt ska bäddas in i Html-dokumentet i Base64-format. Observera att inställning av denna flagga kan avsevärt öka storleken på den genererade Html-filen.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Exempel



Visar hur man bestämmer var inbäddade teckensnitt ska lagras när ett dokument exporteras till Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// När vi exporterar ett dokument med inbäddade teckensnitt till .html,
// Aspose.Words kan placera teckensnitten på två möjliga platser.
// Att sätta flaggan "ExportEmbeddedFonts" till "true" kommer att lagra rådata för inbäddade teckensnitt i CSS-stilmallen,
// i "url"-egenskapen för "@font-face"-regeln. Detta kan skapa en enorm CSS-stilmallsfil
// och minska antalet externa filer som denna HTML-konvertering kommer att skapa.
// Att sätta denna flagga till "false" kommer att skapa en fil för varje teckensnitt.
// CSS-stilmallen kommer att länka till varje teckensnittsfil med hjälp av "url"-egenskapen i "@font-face"-regeln.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
