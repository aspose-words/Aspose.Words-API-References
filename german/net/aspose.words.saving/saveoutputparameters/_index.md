---
title: Class SaveOutputParameters
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.SaveOutputParameters klas. Dieses Objekt wird nach dem Speichern eines Dokuments an den Aufrufer zurückgegeben und enthält zusätzliche Informationen darüber dass während des Speichervorgangs generiert oder berechnet wurde. Der Aufrufer kann dieses Objekt verwenden oder ignorieren.
type: docs
weight: 5590
url: /de/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Dieses Objekt wird nach dem Speichern eines Dokuments an den Aufrufer zurückgegeben und enthält zusätzliche Informationen darüber, dass während des Speichervorgangs generiert oder berechnet wurde. Der Aufrufer kann dieses Objekt verwenden oder ignorieren.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class SaveOutputParameters
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Gibt die Content-Type-Zeichenfolge (Internet Media Type) zurück, die den Typ des gespeicherten Dokuments identifiziert. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


