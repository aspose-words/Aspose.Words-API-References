---
title: TableStyle.ColumnStripe
second_title: Aspose.Words för .NET API Referens
description: TableStyle fast egendom. Hämtar eller ställer in ett antal kolumner som ska inkluderas i bandningen när stilen anger udda/jämna kolumner.
type: docs
weight: 70
url: /sv/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Hämtar eller ställer in ett antal kolumner som ska inkluderas i bandningen när stilen anger udda/jämna kolumner.

```csharp
public int ColumnStripe { get; set; }
```

### Exempel

Visar hur man skapar villkorliga tabellstilar som växlar mellan rader.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan konfigurera en villkorlig stil för en tabell för att tillämpa en annan färg på raden/kolumnen,
// baserat på om raden/kolumnen är jämn eller udda, vilket skapar ett alternerande färgmönster.
// Vi kan också använda ett nummer n på rad-/kolumnbandet,
// betyder att färgen växlar efter var n:e rad/kolumn istället för en.
// Skapa en tabell där enstaka kolumner och rader kommer att banda kolumnerna i tre band.
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

// Tillämpa en linjestil på tabellens alla kanter.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Ställ in de två färgerna, som växlar över var tredje rad.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Ställ in en färg som ska tillämpas på varje jämn kolumn, vilket kommer att åsidosätta alla anpassade radfärger.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// Egenskapen "StyleOptions" aktiverar radband som standard.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Använd egenskapen "StyleOptions" också för att aktivera kolumnband.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Se även

* class [TableStyle](../)
* namnutrymme [Aspose.Words](../../tablestyle/)
* hopsättning [Aspose.Words](../../../)


