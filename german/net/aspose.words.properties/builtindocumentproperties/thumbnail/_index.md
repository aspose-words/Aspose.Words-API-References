---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words für .NET
description: BuiltInDocumentProperties Thumbnail eigendom. Ruft die Miniaturansicht des Dokuments ab oder legt diese fest in C#.
type: docs
weight: 280
url: /de/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Ruft die Miniaturansicht des Dokuments ab oder legt diese fest.

```csharp
public byte[] Thumbnail { get; set; }
```

## Bemerkungen

Derzeit wird diese Eigenschaft nur verwendet, wenn ein Dokument nach ePub exportiert wird. Es wird nicht aus anderen Dokumentformaten gelesen und in diese geschrieben.

Auf diese Eigenschaft kann ein Bild in einem beliebigen Format eingestellt werden, das Format wird jedoch beim Export überprüft. InvalidOperationException wird ausgelöst, wenn das Bild ungültig ist oder sein Format für das -spezifische Dokumentformat nicht unterstützt wird.

Für die ePub-Veröffentlichung können nur GIF-, JPEG- und PNG-Bilder verwendet werden.

## Beispiele

Zeigt, wie man einem Dokument, das wir als Epub speichern, eine Miniaturansicht hinzufügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Wenn wir ein Dokument, dessen „Thumbnail“-Eigenschaft Bilddaten enthält, die wir hinzugefügt haben, als Epub speichern,
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
