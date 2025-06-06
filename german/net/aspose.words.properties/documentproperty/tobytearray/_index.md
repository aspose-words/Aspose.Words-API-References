---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words für .NET
description: Konvertieren Sie DocumentProperty mühelos in ein Byte-Array mit der ToByteArray-Methode. Optimieren Sie die Datenverarbeitung und steigern Sie Ihre Programmiereffizienz!
type: docs
weight: 70
url: /de/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Gibt den Eigenschaftswert als Byte-Array zurück.

```csharp
public byte[] ToByteArray()
```

## Bemerkungen

Löst eine Ausnahme aus, wenn der Eigenschaftstyp nichtByteArray.

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

* class [DocumentProperty](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
