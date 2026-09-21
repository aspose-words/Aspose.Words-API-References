---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold metod"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold metod. Styr vilka teckensnittresurser som behöver delmängdsbildning vid sparande till HTML, MHTML eller EPUB. Standard är %0 i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


Styr vilka teckensnittresurser som behöver delmängdsgenerering när man sparar till HTML, MHTML eller EPUB. Standard är **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Anmärkningar


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Exempel



Visar hur man arbetar med teckensnittsdelmängdsbildning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions‑objekt för att konfigurera teckensnittsdelmängdsbildning.
// Anta att vi sätter flaggan "ExportFontResources" till "true" och även anger en mapp i egenskapen "FontsFolder".
// I så fall kommer sparningsoperationen att skapa den mappen och placera en .ttf‑fil i den.
// den mappen för varje teckensnitt som vårt dokument använder.
// Varje .ttf‑fil kommer att innehålla hela teckensnittets glyfuppsättning,
// vilket potentiellt kan resultera i en mycket stor fil som följer med dokumentet.
// När vi tillämpar delmängdsbildning på ett teckensnitt kommer dess exporterade rådata endast att innehålla de glyfer som dokumentet är
// i bruk istället för hela glyfuppsättningen. Om texten i vårt dokument bara använder en liten del av ett teckensnitts
// glyfuppsättning, kommer delmängdsbildning att avsevärt minska storleken på våra utdata‑dokument.
// Vi kan använda egenskapen "FontResourcesSubsettingSizeThreshold" för att definiera en .ttf‑filstorlek, i byte.
// Om ett exporterat teckensnitt skapar en fil som är större än så, kommer sparningsoperationen att tillämpa delmängdsbildning på det teckensnittet.
// Att sätta ett tröskelvärde på 0 tillämpar delmängdsbildning på alla teckensnitt,
// och att sätta det till "int.MaxValue" inaktiverar i praktiken delmängdsbildning.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // Som standard kommer .ttf‑filerna för var och en av våra tre teckensnitt att vara över 700 MB.
    // Delmängdsbildning kommer att minska dem alla till under 30 MB.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
