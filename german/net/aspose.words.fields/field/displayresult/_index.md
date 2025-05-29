---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Field DisplayResult“, die den Text für Ihre angezeigten Feldergebnisse liefert und so die Übersichtlichkeit und das Benutzererlebnis verbessert.
type: docs
weight: 10
url: /de/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Ruft den Text ab, der das angezeigte Feldergebnis darstellt.

```csharp
public string DisplayResult { get; }
```

## Bemerkungen

Die[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) Methode muss aufgerufen werden, um den korrekten Wert für the zu erhalten[`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) Und[`FieldAutoNumLgl`](../../fieldautonumlgl/) Felder.

## Beispiele

Zeigt, wie der tatsächliche Text abgerufen wird, der in einem Feld im Dokument angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Wir können die DisplayResult-Eigenschaft verwenden, um zu überprüfen, welcher genaue Text
// An seiner Stelle im Dokument würde ein Feld angezeigt.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

    // Felder behalten in Echtzeit keine genauen Ergebniswerte bei.
// Um sicherzustellen, dass unsere Felder jederzeit genaue Ergebnisse anzeigen,
// beispielsweise direkt vor einem Speichervorgang. Wir müssen sie manuell aktualisieren.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
