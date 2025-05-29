---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.HeightRule für die präzise Steuerung der Objekthöhe in Dokumenten. Optimieren Sie Ihren Workflow mit dieser wichtigen Funktion!
type: docs
weight: 3560
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
| AtLeast | `0` | Die Höhe entspricht mindestens der angegebenen Höhe in Punkten. Sie wird bei Bedarf erweitert, um den gesamten Text in einem Objekt unterzubringen. |
| Exactly | `1` | Die Höhe wird exakt in Punkten angegeben. Bitte beachten Sie: Wenn der Text nicht in das Objekt dieser Höhe passt, wird er abgeschnitten angezeigt. |
| Auto | `2` | Die Höhe wird automatisch angepasst, um den gesamten Text in einem Objekt unterzubringen. |

## Beispiele

Zeigt, wie Zeilen mit einem Dokumentgenerator formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Starten Sie eine zweite Zeile und konfigurieren Sie dann deren Höhe. Der Builder wendet diese Einstellungen an auf
// seine aktuelle Zeile sowie alle neuen Zeilen, die es danach erstellt.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Die erste Zeile wurde durch die Neukonfiguration der Auffüllung nicht beeinflusst und enthält weiterhin die Standardwerte.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
