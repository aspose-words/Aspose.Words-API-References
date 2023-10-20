---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ResourceFolderAlias fast egendom. Anger namnet på mappen som används för att konstruera URIer för alla resurser som skrivits in i ett HTMLdokument. Standard är en tom sträng i C#.
type: docs
weight: 430
url: /sv/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Anger namnet på mappen som används för att konstruera URI:er för alla resurser som skrivits in i ett HTML-dokument. Standard är en tom sträng.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Anmärkningar

`ResourceFolderAlias` är det enklaste sättet att specificera hur URI:er för alla resursfiler ska vara konstruerade. Samma information kan anges för bilder och typsnitt separat via[`ImagesFolderAlias`](../imagesfolderalias/) och[`FontsFolderAlias`](../fontsfolderalias/) respektive fastigheter. Det finns dock ingen enskild egenskap för CSS.

`ResourceFolderAlias` har lägre prioritet än[`FontsFolderAlias`](../fontsfolderalias/) och[`ImagesFolderAlias`](../imagesfolderalias/) . Till exempel om båda`ResourceFolderAlias` och[`FontsFolderAlias`](../fontsfolderalias/) är specificerade, kommer teckensnittens URI:er att konstrueras med [`FontsFolderAlias`](../fontsfolderalias/) , medan URI:er för bilder och CSS kommer att konstrueras med `ResourceFolderAlias`.

Om`ResourceFolderAlias` är tom, den[`ResourceFolder`](../resourcefolder/)egenskapsvärdet kommer att användas för att konstruera resurs-URI:er.

Om`ResourceFolderAlias` är satt till '.' (prick), kommer resurs-URI endast att innehålla filnamn, utan någon sökväg.

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
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resurser",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
