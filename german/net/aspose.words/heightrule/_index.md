---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words für .NET
description: Aspose.Words.HeightRule opsomming. Gibt die Regel zur Bestimmung der Höhe eines Objekts an in C#.
type: docs
weight: 3130
url: /de/net/aspose.words/heightrule/
---
## HeightRule enumeration

Gibt die Regel zur Bestimmung der Höhe eines Objekts an.

```csharp
public enum HeightRule
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AtLeast | `0` | Die Höhe entspricht mindestens der angegebenen Höhe in Punkten. Bei Bedarf wird es vergrößert, , um den gesamten Text in einem Objekt unterzubringen. |
| Exactly | `1` | Die Höhe wird exakt in Punkten angegeben. Bitte beachten Sie, dass der Text abgeschnitten angezeigt wird, wenn er nicht in das Objekt dieser Höhe passt. |
| Auto | `2` | Die Höhe wird automatisch vergrößert, um den gesamten Text innerhalb eines Objekts aufzunehmen. |

## Beispiele

Zeigt, wie Zeilen mit einem Document Builder formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Eine zweite Zeile beginnen und dann deren Höhe konfigurieren. Der Builder wendet diese Einstellungen an
// seine aktuelle Zeile sowie alle danach erstellten neuen Zeilen.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Die erste Zeile war von der Neukonfiguration der Auffüllung nicht betroffen und enthält weiterhin die Standardwerte.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
