---
title: MarkdownSaveOptions.ImagesFolder
second_title: Aspose.Words für .NET-API-Referenz
description: MarkdownSaveOptions eigendom. Gibt den physischen Ordner an in dem Bilder gespeichert werden wenn ein Dokument nach exportiert wirdMarkdown Format. Standard ist eine leere Zeichenfolge.
type: docs
weight: 40
url: /de/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument nach exportiert wirdMarkdown Format. Standard ist eine leere Zeichenfolge.

```csharp
public string ImagesFolder { get; set; }
```

### Bemerkungen

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) InMarkdownformat, Aspose.Words muss alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. `ImagesFolder` ermöglicht Ihnen festzulegen, wo die Bilder gespeichert werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die Bilder standardmäßig in demselben Ordner, in dem die Dokumentdatei gespeichert ist. Verwenden`ImagesFolder` um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words nicht über einen Ordner , in dem die Bilder gespeichert werden sollen, die Bilder müssen jedoch trotzdem irgendwo gespeichert werden. In diesem Fall müssen Sie einen zugänglichen Ordner im angeben`ImagesFolder` Eigenschaft.

Wenn der von angegebene Ordner`ImagesFolder` existiert nicht, es wird automatisch erstellt.

### Beispiele

Zeigt, wie der Name des Ordners angegeben wird, der zum Erstellen von Bild-URIs verwendet wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Mit der Eigenschaft „ImagesFolder“ einen Ordner im lokalen Dateisystem zuweisen, in den
// Aspose.Words speichert alle verknüpften Bilder des Dokuments.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Verwenden Sie die Eigenschaft „ImagesFolderAlias“, um diesen Ordner zu verwenden
// beim Erstellen von Bild-URIs anstelle des Namens des Bilderordners.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

Zeigt, wie der Name des Ordners angegeben wird, der zum Erstellen von Bild-URIs verwendet wird (.NetStandard 2.0).

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Mit der Eigenschaft „ImagesFolder“ einen Ordner im lokalen Dateisystem zuweisen, in den
// Aspose.Words speichert alle verknüpften Bilder des Dokuments.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Verwenden Sie die Eigenschaft „ImagesFolderAlias“, um diesen Ordner zu verwenden
// beim Erstellen von Bild-URIs anstelle des Namens des Bilderordners.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Siehe auch

* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../markdownsaveoptions/)
* Montage [Aspose.Words](../../../)


