---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „MarkdownSaveOptions ImagesFolderAlias“, um Bild-URIs in Ihren Dokumenten einfach zu verwalten. Optimieren Sie Ihren Workflow mit dieser wichtigen Funktion!
type: docs
weight: 90
url: /de/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen der in ein Dokument geschriebenen Bild-URIs verwendet wird. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Bemerkungen

Wenn Sie eine[`Document`](../../../aspose.words/document/) InMarkdown Format, Aspose.Words muss alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [`ImagesFolder`](../imagesfolder/) ermöglicht Ihnen, festzulegen, wo die Bilder gespeichert werden sollen und `ImagesFolderAlias` ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn`ImagesFolderAlias` ist keine leere Zeichenfolge, dann wird die Bild-URI geschrieben zu MarkdownImagesFolderAlias + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` ist eine leere Zeichenfolge, dann wird die Bild-URI geschrieben zu MarkdownImagesFolder + &lt;Bilddateiname&gt;.

Wenn`ImagesFolderAlias` auf ‚.‘ (Punkt) gesetzt ist, dann wird der Bilddateiname ohne Pfad in Markdown geschrieben, unabhängig von anderen Optionen.

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
