---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words för .NET
description: Upptäck hur HtmlSaveOptions ExportCidUrlsForMhtmlResources förbättrar MHTML-dokument genom att aktivera CID-URL:er för bilder, teckensnitt och CSS. Standardvärdet är falskt.
type: docs
weight: 110
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

Anger om CID-URL:er (Content-ID) ska användas för att referera till resurser (bilder, teckensnitt, CSS) som ingår i MHTML -dokument. Standardvärdet är`falsk` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Anmärkningar

Det här alternativet påverkar endast dokument som sparas i MHTML.

Som standard refereras resurser i MHTML-dokument med filnamn (till exempel "image.png"), vilket matchas mot "Content-Location"-rubriker i MIME-delar.

Det här alternativet möjliggör en alternativ metod, där referenser till resursfiler skrivs som CID (Content-ID) -URL:er (till exempel "cid:image.png") och matchas mot "Content-ID"-rubriker.

teorin borde det inte finnas någon skillnad mellan de två refereringsmetoderna och endera av dem borde fungera utan problem i alla webbläsare eller e-postagenter. I praktiken misslyckas dock vissa agenter med att hämta resurser efter filnamn. Om din webbläsare eller e-postagent vägrar att ladda resurser som ingår i ett MTHML-dokument (inte visar bilder eller inte laddar CSS-stilar), försök att exportera dokumentet med CID-URL:er.

## Exempel

Visar hur man aktiverar innehålls-ID:n för utdata från MHTML-dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Om du ställer in den här flaggan ersätts taggarna "Content-Location"
// med "Content-ID"-taggar för varje resurs från indatadokumentet.
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
