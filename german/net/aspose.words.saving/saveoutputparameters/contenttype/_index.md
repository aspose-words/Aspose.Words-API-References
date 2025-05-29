---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words für .NET
description: Entdecken Sie die ContentType-Eigenschaft von SaveOutputParameters, die den Internetmedientyp für Ihre gespeicherten Dokumente bereitstellt und so eine genaue Dateiidentifizierung gewährleistet.
type: docs
weight: 10
url: /de/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Gibt die Inhaltstypzeichenfolge (Internetmedientyp) zurück, die den Typ des gespeicherten Dokuments identifiziert.

```csharp
public string ContentType { get; }
```

## Beispiele

Zeigt, wie auf die Ausgabeparameter des Speichervorgangs eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Nachdem wir ein Dokument gespeichert haben, können wir auf den Internetmedientyp (MIME-Typ) des neu erstellten Ausgabedokuments zugreifen.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Diese Eigenschaft ändert sich je nach Speicherformat.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Siehe auch

* class [SaveOutputParameters](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
