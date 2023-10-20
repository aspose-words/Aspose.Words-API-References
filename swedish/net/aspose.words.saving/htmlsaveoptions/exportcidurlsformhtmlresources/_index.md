---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ExportCidUrlsForMhtmlResources fast egendom. Anger om CIDwebbadresser ContentID ska användas för att referera till resurser bilder teckensnitt CSS som ingår i MHTML dokument. Standardvärdet ärfalsk  i C#.
type: docs
weight: 110
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

Anger om CID-webbadresser (Content-ID) ska användas för att referera till resurser (bilder, teckensnitt, CSS) som ingår i MHTML -dokument. Standardvärdet är`falsk` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Anmärkningar

Det här alternativet påverkar endast dokument som sparas i MHTML.

Som standard refereras till resurser i MHTML-dokument med filnamn (till exempel "image.png"), vilka matchas mot "Content-Location"-rubriker för MIME-delar.

Det här alternativet möjliggör en alternativ metod, där referenser till resursfiler skrivs som CID (Content-ID) URLs (till exempel "cid:image.png") och matchas mot "Content-ID"-rubriker.

teorin borde det inte finnas någon skillnad mellan de två refereringsmetoderna och någon av dem ska fungera bra i vilken webbläsare eller e-postagent som helst. I praktiken misslyckas dock vissa agenter med att hämta resurser efter filnamn. Om din webbläsare eller e-postagent vägrar att ladda resurser som ingår i ett MTHML-dokument (inte visar bilder eller inte load CSS-stilar), försök att exportera dokumentet med CID-URL:er.

## Exempel

Visar hur man aktiverar innehålls-ID för MHTML-utdatadokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Att ställa in denna flagga kommer att ersätta "Content-Location"-taggar
// med "Content-ID"-taggar för varje resurs från inmatningsdokumentet.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
