---
title: SaveOutputParameters.ContentType
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOutputParameters eigendom. Gibt die ContentTypeZeichenfolge Internet Media Type zurück die den Typ des gespeicherten Dokuments identifiziert.
type: docs
weight: 10
url: /de/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Gibt die Content-Type-Zeichenfolge (Internet Media Type) zurück, die den Typ des gespeicherten Dokuments identifiziert.

```csharp
public string ContentType { get; }
```

### Beispiele

Zeigt, wie auf Ausgabeparameter des Speichervorgangs eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Nachdem wir ein Dokument gespeichert haben, können wir auf den Internet Media Type (MIME-Typ) des neu erstellten Ausgabedokuments zugreifen.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Diese Eigenschaft ändert sich je nach Speicherformat.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Siehe auch

* class [SaveOutputParameters](../)
* namensraum [Aspose.Words.Saving](../../saveoutputparameters/)
* Montage [Aspose.Words](../../../)


