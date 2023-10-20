---
title: FieldAdvance.VerticalPosition
linktitle: VerticalPosition
articleTitle: VerticalPosition
second_title: Aspose.Words für .NET
description: FieldAdvance VerticalPosition eigendom. Ruft die Anzahl der Punkte ab oder legt diese fest um die der Text der auf das Feld folgt vertikal vom oberen Rand der Seite verschoben werden soll in C#.
type: docs
weight: 70
url: /de/net/aspose.words.fields/fieldadvance/verticalposition/
---
## FieldAdvance.VerticalPosition property

Ruft die Anzahl der Punkte ab oder legt diese fest, um die der Text, der auf das Feld folgt, vertikal vom oberen Rand der Seite verschoben werden soll.

```csharp
public string VerticalPosition { get; set; }
```

## Beispiele

Zeigt, wie man ein ADVANCE-Feld einfügt und seine Eigenschaften bearbeitet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Im Folgenden finden Sie zwei Möglichkeiten, das ADVANCE-Feld zu verwenden, um die Position des darauf folgenden Textes anzupassen.
// Die Auswirkungen eines ADVANCE-Feldes werden weiterhin angewendet, bis der Absatz endet.
// oder ein anderes ADVANCE-Feld aktualisiert die Offset-/Koordinatenwerte.
// 1 – Geben Sie einen Richtungsoffset an:
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
