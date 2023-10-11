---
title: Enum ConditionalStyleType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.ConditionalStyleType opsomming. Stellt mögliche Tabellenbereiche dar für die eine bedingte Formatierung in einem Tabellenstil definiert werden kann.
type: docs
weight: 330
url: /de/net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

Stellt mögliche Tabellenbereiche dar, für die eine bedingte Formatierung in einem Tabellenstil definiert werden kann.

```csharp
public enum ConditionalStyleType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FirstRow | `0` | Gibt die Formatierung der ersten Zeile einer Tabelle an. |
| FirstColumn | `1` | Gibt die Formatierung der ersten Spalte einer Tabelle an. |
| LastRow | `2` | Gibt die Formatierung der letzten Zeile einer Tabelle an. |
| LastColumn | `3` | Gibt die Formatierung der letzten Spalte einer Tabelle an. |
| OddRowBanding | `4` | Gibt die Formatierung des ungeradzahligen Zeilenstreifens an. |
| OddColumnBanding | `5` | Gibt die Formatierung des ungeradzahligen Spaltenstripes an. |
| EvenRowBanding | `6` | Gibt die Formatierung des geradzahligen Zeilenstreifens an. |
| EvenColumnBanding | `7` | Gibt die Formatierung des geradzahligen Spaltenstripes an. |
| TopLeftCell | `8` | Gibt die Formatierung der oberen linken Zelle einer Tabelle an. |
| TopRightCell | `9` | Gibt die Formatierung der oberen rechten Zelle einer Tabelle an. |
| BottomLeftCell | `10` | Gibt die Formatierung der unteren linken Zelle einer Tabelle an. |
| BottomRightCell | `11` | Gibt die Formatierung der unteren rechten Zelle einer Tabelle an. |

### Beispiele

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

// Einen benutzerdefinierten Tabellenstil erstellen.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Bedingte Stile sind Formatierungsänderungen, die sich nur auf einige Zellen der Tabelle auswirken
// basierend auf einem Prädikat, z. B. den Zellen in der letzten Zeile.
// Nachfolgend finden Sie drei Möglichkeiten, auf die bedingten Stile eines Tabellenstils aus der „ConditionalStyles“-Sammlung zuzugreifen.
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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


