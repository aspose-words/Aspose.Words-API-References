---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „MarkdownSaveOptions ImagesFolder“ Ihre Dokumentexporte verbessert, indem sie den idealen Ordner zum Speichern von Bildern im Markdown-Format angibt.
type: docs
weight: 80
url: /de/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument in exportiert wird.Markdown Format. Standard ist eine leere Zeichenfolge.

```csharp
public string ImagesFolder { get; set; }
```

## Bemerkungen

Wenn Sie ein[`Document`](../../../aspose.words/document/) InMarkdownFormat, Aspose.Words muss alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. `ImagesFolder` ermöglicht Ihnen, anzugeben, wo die Bilder gespeichert werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die Bilder standardmäßig im selben Ordner wie die Dokumentdatei. Verwenden Sie`ImagesFolder` um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words nicht über einen Ordner , in dem die Bilder gespeichert werden können, sondern muss die Bilder trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner im`ImagesFolder` Eigenschaft.

Wenn der Ordner angegeben durch`ImagesFolder` nicht existiert, wird es automatisch erstellt.

## Beispiele

Zeigt, wie der Name des Ordners angegeben wird, der zum Erstellen von Bild-URIs verwendet wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Verwenden Sie die Eigenschaft "ImagesFolder", um einen Ordner im lokalen Dateisystem zuzuweisen, in den
// Aspose.Words speichert alle verknüpften Bilder des Dokuments.
saveOptions.ImagesFolder = imagesFolder;
// Verwenden Sie die Eigenschaft „ImagesFolderAlias“, um diesen Ordner zu verwenden
// beim Erstellen von Bild-URIs anstelle des Namens des Bilderordners.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Siehe auch

* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
