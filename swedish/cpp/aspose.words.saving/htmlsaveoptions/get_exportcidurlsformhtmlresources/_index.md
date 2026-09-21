---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources metod"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources metod. Anger om CID (Content-ID)-URL:er ska användas för att referera till resurser (bilder, teckensnitt, CSS) som ingår i MHTML-dokument. Standardvärdet är false i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


Anger om CID (Content-ID)-URL:er ska användas för att referera resurser (bilder, teckensnitt, CSS) som ingår i MHTML‑dokument. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Anmärkningar


Detta alternativ påverkar endast dokument som sparas till MHTML.

Som standard refereras resurser i MHTML-dokument med filnamn (till exempel \"image.png\"), som matchas mot \"Content-Location\"-rubriker i MIME-delar.

Det här alternativet aktiverar en alternativ metod, där referenser till resursfiler skrivs som CID (Content-ID)-URL:er (till exempel \"cid:image.png\") och matchas mot \"Content-ID\"-rubriker.

I teorin bör det inte finnas någon skillnad mellan de två referensmetoderna och någon av dem bör fungera bra i vilken webbläsare eller e-postklient som helst. I praktiken misslyckas dock vissa klienter med att hämta resurser via filnamn. Om din webbläsare eller e-postklient vägrar att ladda resurser som ingår i ett MTHML-dokument (visar inte bilder eller laddar inte CSS-stilar), försök exportera dokumentet med CID-URL:er.

## Exempel



Visar hur man aktiverar innehålls-ID:n för utdata-MHTML-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Att sätta den här flaggan kommer att ersätta \"Content-Location\"-taggar
// med \"Content-ID\"-taggar för varje resurs från indatadokumentet.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
