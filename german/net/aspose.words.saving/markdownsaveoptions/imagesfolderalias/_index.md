---
title: MarkdownSaveOptions.ImagesFolderAlias
second_title: Aspose.Words für .NET-API-Referenz
description: MarkdownSaveOptions eigendom. Gibt den Namen des Ordners an der zum Erstellen von BildURIs verwendet wird die in ein Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge.
type: docs
weight: 50
url: /de/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Bemerkungen

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) InMarkdown format, Aspose.Words muss alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [`ImagesFolder`](../imagesfolder/) ermöglicht Ihnen festzulegen, wo die Bilder gespeichert werden und `ImagesFolderAlias` ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn`ImagesFolderAlias` ist kein leerer String, dann wird der Bild-URI in Markdown geschrieben ImagesFolderAlias + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` Ist ein leerer String, dann wird der Bild-URI in Markdown geschriebenImagesFolder + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias`ist eingestellt auf '.' (Punkt), dann wird die Bilddatei name unabhängig von anderen Optionen ohne Pfad in Markdown geschrieben.

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


