---
title: HtmlSaveOptions.ImagesFolderAlias
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt den Namen des Ordners an der zum Erstellen von BildURIs verwendet wird die in ein HTMLDokument geschrieben werden. Standard ist eine leere Zeichenfolge.
type: docs
weight: 380
url: /de/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standard ist eine leere Zeichenfolge.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Bemerkungen

Beim Speichern von a[`Document`](../../../aspose.words/document/) im HTML-Format muss Aspose.Words alle in das Dokument eingebetteten -Bilder als eigenständige Dateien speichern.[`ImagesFolder`](../imagesfolder/) Mit können Sie angeben, wo die Bilder gespeichert werden und`ImagesFolderAlias` ermöglicht die Angabe, wie die Bild-URIs aufgebaut werden.

Wenn`ImagesFolderAlias`kein leerer String ist, dann wird die Bild-URI in HTML geschrieben ImagesFolderAlias + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` ein leerer String ist, dann wird die Bild-URI in HTML geschriebenImagesFolder + &lt;Name der Bilddatei&gt;.

Wenn`ImagesFolderAlias` ist eingestellt auf '.' (Punkt), dann wird der Bilddateiname unabhängig von anderen Optionen ohne Pfad in HTML geschrieben.

Alternativ kann der Name des Ordners zum Erstellen von Bild-URIs angegeben werden[`ResourceFolderAlias`](../resourcefolderalias/).

### Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words erstellt, wenn ein Dokument in HTML gespeichert wird.

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
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


