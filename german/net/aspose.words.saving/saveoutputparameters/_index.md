---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.SaveOutputParameters, die wichtige Details nach dem Speichern des Dokuments bereitstellt und so Ihr Dokumentenverwaltungserlebnis verbessert.
type: docs
weight: 6390
url: /de/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Dieses Objekt wird nach dem Speichern eines Dokuments an den Aufrufer zurückgegeben und enthält zusätzliche Informationen, die während des Speichervorgangs generiert oder berechnet wurden. Der Aufrufer kann dieses Objekt verwenden oder ignorieren.

Um mehr zu erfahren, besuchen Sie die[Speichern eines Dokuments](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class SaveOutputParameters
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Gibt die Inhaltstypzeichenfolge (Internetmedientyp) zurück, die den Typ des gespeicherten Dokuments identifiziert. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
