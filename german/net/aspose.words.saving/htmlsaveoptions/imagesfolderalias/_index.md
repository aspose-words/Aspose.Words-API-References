---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „HtmlSaveOptions ImagesFolderAlias“ zur einfachen Verwaltung von Bild-URIs in Ihren HTML-Dokumenten. Vereinfachen Sie Ihren Workflow mit dieser wichtigen Funktion!
type: docs
weight: 370
url: /de/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Bemerkungen

Wenn Sie eine[`Document`](../../../aspose.words/document/) Im HTML-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.[`ImagesFolder`](../imagesfolder/) ermöglicht Ihnen, festzulegen, wo die Bilder gespeichert werden und`ImagesFolderAlias` ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn`ImagesFolderAlias` ist keine leere Zeichenfolge, dann wird die Bild-URI geschrieben zu HTML wirdImagesFolderAlias + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias`ist eine leere Zeichenfolge, dann wird die Bild-URI geschrieben zu HTML wirdImagesFolder + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` auf „.“ (Punkt) gesetzt ist, wird der Bilddateiname ohne Pfad in HTML geschrieben, unabhängig von anderen Optionen.

Alternativ können Sie den Namen des Ordners angeben, um Bild-URIs zu erstellen. Verwenden Sie dazu[`ResourceFolderAlias`](../resourcefolderalias/).

## Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments im HTML-Format erstellt.

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
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
