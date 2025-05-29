---
title: TableStyle.RowStripe
linktitle: RowStripe
articleTitle: RowStripe
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TableStyle RowStripe för att enkelt anpassa udda/jämna rader för förbättrad läsbarhet och visuell tilltalning i tabellen.
type: docs
weight: 120
url: /sv/net/aspose.words/tablestyle/rowstripe/
---
## TableStyle.RowStripe property

Hämtar eller anger ett antal rader som ska inkluderas i bandningen när stilen anger udda/jämna radband.

```csharp
public int RowStripe { get; set; }
```

## Exempel

Visar hur man skapar villkorliga tabellformat som växlar mellan rader.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan konfigurera en villkorlig stil för en tabell för att tillämpa en annan färg på raden/kolumnen,
// baserat på om raden/kolumnen är jämn eller udda, vilket skapar ett alternerande färgmönster.
// Vi kan också tillämpa ett tal n på rad-/kolumnbandningen,
// vilket betyder att färgen alternerar efter var n:te rad/kolumn istället för en.
// Skapa en tabell där enskilda kolumner och rader är uppdelade i band, kolumnerna är uppdelade i tre.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Använd en linjestil på alla tabellens kanter.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Ställ in de två färgerna, som växlar över var tredje rad.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Ange en färg som ska tillämpas på varje jämn kolumn, vilket åsidosätter eventuell anpassad radfärgning.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// Egenskapen "StyleOptions" aktiverar radbandning som standard.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Använd även egenskapen "StyleOptions" för att aktivera kolumnbandning.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Se även

* class [TableStyle](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
