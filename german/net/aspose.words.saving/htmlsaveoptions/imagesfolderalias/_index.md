---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ImagesFolderAlias eigendom. Gibt den Namen des Ordners an der zum Erstellen von BildURIs verwendet wird die in ein HTMLDokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge in C#.
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

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) Im HTML-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.[`ImagesFolder`](../imagesfolder/) Mit können Sie angeben, wo die Bilder gespeichert werden`ImagesFolderAlias` ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn`ImagesFolderAlias` kein leerer String ist, wird der Bild-URI in HTML geschrieben angezeigtImagesFolderAlias + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` eine leere Zeichenfolge ist, wird der Bild-URI in HTML geschriebenImagesFolder + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias`ist eingestellt auf '.' (Punkt), dann wird der Bilddateiname unabhängig von anderen Optionen ohne Pfad in HTML geschrieben.

Eine alternative Möglichkeit, den Namen des Ordners anzugeben, um Bild-URIs zu erstellen, ist die Verwendung[`ResourceFolderAlias`](../resourcefolderalias/).

## Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments in HTML erstellt.

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
