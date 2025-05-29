---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words för .NET
description: Optimera dina HTML-dokument med egenskapen HtmlSaveOptions ResourceFolderAlias, som definierar mappnamn för effektiv URI-konstruktion av resurser.
type: docs
weight: 450
url: /sv/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Anger namnet på den mapp som används för att konstruera URI:er för alla resurser som skrivs in i ett HTML-dokument. Standardvärdet är en tom sträng.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Anmärkningar

`ResourceFolderAlias` är det enklaste sättet att ange hur URI:er för alla resursfiler ska konstrueras. Samma information kan anges separat för bilder och teckensnitt via[`ImagesFolderAlias`](../imagesfolderalias/) och[`FontsFolderAlias`](../fontsfolderalias/) egenskaper, respektive. Det finns dock ingen individuell egenskap för CSS.

`ResourceFolderAlias` har lägre prioritet än[`FontsFolderAlias`](../fontsfolderalias/) och[`ImagesFolderAlias`](../imagesfolderalias/) Till exempel, om båda`ResourceFolderAlias` och[`FontsFolderAlias`](../fontsfolderalias/) anges, kommer teckensnittens URI:er att konstrueras med hjälp av [`FontsFolderAlias`](../fontsfolderalias/) medan URI:er för bilder och CSS kommer att konstrueras med hjälp av `ResourceFolderAlias`.

Om`ResourceFolderAlias` är tom, den[`ResourceFolder`](../resourcefolder/) egenskapsvärdet kommer att användas för att konstruera resurs-URI:er.

Om`ResourceFolderAlias` är satt till '.' (punkt), kommer resurs-URI:er endast att innehålla filnamn, utan någon sökväg.

## Exempel

Visar hur man ställer in mappar och mappalias för externt sparade resurser som Aspose.Words skapar när ett dokument sparas till HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/bilder",
    ResourceFolderAlias = "http://example.com/resurser",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
