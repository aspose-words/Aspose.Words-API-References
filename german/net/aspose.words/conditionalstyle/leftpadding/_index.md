---
title: ConditionalStyle.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words für .NET
description: Entdecken Sie die ConditionalStyle LeftPadding-Eigenschaft, um den linken Abstand in Tabellenzellen einfach anzupassen. Verbessern Sie Ihre Layouts mit präziser Kontrolle!
type: docs
weight: 40
url: /de/net/aspose.words/conditionalstyle/leftpadding/
---
## ConditionalStyle.LeftPadding property

Ruft den Abstand (in Punkten) ab, der links vom Inhalt der Tabellenzellen hinzugefügt werden soll, oder legt diesen fest.

```csharp
public double LeftPadding { get; set; }
```

## Beispiele

Zeigt, wie mit bestimmten Bereichsstilen einer Tabelle gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Erstellen Sie einen benutzerdefinierten Tabellenstil.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Bedingte Stile sind Formatierungsänderungen, die nur einige Zellen der Tabelle betreffen
// basierend auf einem Prädikat, z. B. dass sich die Zellen in der letzten Zeile befinden.
// Unten sind drei Möglichkeiten aufgeführt, um auf die bedingten Stile eines Tabellenstils aus der Sammlung „ConditionalStyles“ zuzugreifen.
// 1 - Nach Stiltyp:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Nach Index:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Als Eigenschaft:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Auffüllung und Textformatierung auf bedingte Stile anwenden.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Alle möglichen Stilbedingungen auflisten.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Den benutzerdefinierten Stil, der alle bedingten Stile enthält, auf die Tabelle anwenden.
table.Style = tableStyle;

// Unser Stil wendet standardmäßig einige bedingte Stile an.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Alle anderen Stile müssen wir selbst über die Eigenschaft „StyleOptions“ aktivieren.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Siehe auch

* class [ConditionalStyle](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
