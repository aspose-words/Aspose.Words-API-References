---
title: FieldAdvance.HorizontalPosition
linktitle: HorizontalPosition
articleTitle: HorizontalPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldAdvance HorizontalPosition-Eigenschaft und passen Sie die Textpositionierung für eine präzise Layoutsteuerung in Ihren Dokumenten einfach an. Verbessern Sie noch heute Ihre Formatierung!
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldadvance/horizontalposition/
---
## FieldAdvance.HorizontalPosition property

Ruft die Anzahl der Punkte ab oder legt sie fest, um die der Text, der dem Feld folgt, horizontal vom linken Rand der Spalte, des Rahmens oder des Textfelds verschoben werden soll.

```csharp
public string HorizontalPosition { get; set; }
```

## Beispiele

Zeigt, wie Sie ein ADVANCE-Feld einfügen und seine Eigenschaften bearbeiten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Unten sind zwei Möglichkeiten aufgeführt, wie Sie mit dem Feld ADVANCE die Position des darauf folgenden Textes anpassen können.
// Die Auswirkungen eines ADVANCE-Feldes bleiben bis zum Ende des Absatzes bestehen,
// oder ein anderes ADVANCE-Feld aktualisiert die Offset-/Koordinatenwerte.
// 1 - Geben Sie einen Richtungsversatz an:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Text an eine durch Koordinaten angegebene Position verschieben:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Siehe auch

* class [FieldAdvance](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
