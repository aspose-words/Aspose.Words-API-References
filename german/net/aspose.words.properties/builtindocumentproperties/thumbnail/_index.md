---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words für .NET
description: Verwalten Sie die visuelle Darstellung Ihres Dokuments mit BuiltInDocumentProperties. Erstellen oder legen Sie ganz einfach Miniaturbilder für eine verbesserte Präsentation und Organisation fest.
type: docs
weight: 310
url: /de/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Ruft die Miniaturansicht des Dokuments ab oder legt sie fest.

```csharp
public byte[] Thumbnail { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidOperationException | Wird ausgelöst, wenn das Bild ungültig ist oder sein Format für ein bestimmtes Dokumentformat nicht unterstützt wird. |

## Bemerkungen

Derzeit wird diese Eigenschaft nur verwendet, wenn ein Dokument in ePub exportiert wird. Es wird nicht aus anderen Dokumentformaten gelesen oder in diese geschrieben.

Für diese Eigenschaft kann ein Bild beliebigen Formats festgelegt werden, das Format wird jedoch beim Export überprüft.

Für die ePub-Veröffentlichung können nur GIF-, JPEG- und PNG-Bilder verwendet werden.

## Beispiele

Zeigt, wie einem Dokument, das wir als Epub speichern, eine Miniaturansicht hinzugefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Wenn wir ein Dokument, dessen Eigenschaft „Thumbnail“ Bilddaten enthält, die wir hinzugefügt haben, als Epub speichern,
// Ein Reader, der dieses Dokument öffnet, zeigt das Bild möglicherweise vor der ersten Seite an.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Wir können das Miniaturbild eines Dokuments extrahieren und im lokalen Dateisystem speichern.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
