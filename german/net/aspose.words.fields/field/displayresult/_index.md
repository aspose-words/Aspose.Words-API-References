---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words für .NET
description: Field DisplayResult eigendom. Ruft den Text ab der das angezeigte Feldergebnis darstellt in C#.
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

Die[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) Die Methode muss aufgerufen werden, um den korrekten Wert für the zu erhalten.[`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) Und[`FieldAutoNumLgl`](../../fieldautonumlgl/) Felder.

## Beispiele

Zeigt, wie man den tatsächlichen Text erhält, den ein Feld im Dokument anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Wir können die DisplayResult-Eigenschaft verwenden, um den genauen Text zu überprüfen
// ein Feld würde an seiner Stelle im Dokument angezeigt.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // Felder behalten keine genauen Ergebniswerte in Echtzeit bei.
// Um sicherzustellen, dass unsere Felder jederzeit genaue Ergebnisse anzeigen,
// z. B. direkt vor einem Speichervorgang müssen wir sie manuell aktualisieren.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
