---
title: ConditionalStyle.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words für .NET
description: Müheloses Formatieren mit der ConditionalStyle ClearFormatting-Methode. Vereinfachen Sie Ihren Designprozess und verbessern Sie die Dokumentübersicht noch heute!
type: docs
weight: 100
url: /de/net/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle.ClearFormatting method

Löscht die Formatierung dieses bedingten Stils.

```csharp
public void ClearFormatting()
```

## Beispiele

Zeigt, wie bedingte Tabellenstile zurückgesetzt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// Legen Sie den Tabellenstil fest, um die Ränder der ersten Tabellenzeile rot einzufärben.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Legen Sie den Tabellenstil fest, um die Ränder der letzten Tabellenzeile blau einzufärben.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Unten sind zwei Möglichkeiten aufgeführt, wie Sie mit der Methode „ClearFormatting“ die bedingten Stile löschen können.
// 1 – Löschen Sie die bedingten Stile für einen bestimmten Teil einer Tabelle:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Löschen Sie die bedingten Stile für die gesamte Tabelle:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Siehe auch

* class [ConditionalStyle](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
