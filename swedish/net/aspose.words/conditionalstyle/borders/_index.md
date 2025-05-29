---
title: ConditionalStyle.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words för .NET
description: Utforska egenskapen ConditionalStyle Borders för att komma åt viktiga standardcellkantlinjer och förbättra din design med anpassningsbara stilar för bättre visuella effekter.
type: docs
weight: 10
url: /sv/net/aspose.words/conditionalstyle/borders/
---
## ConditionalStyle.Borders property

Hämtar samlingen av standardcellkantlinjer för den villkorliga stilen.

```csharp
public BorderCollection Borders { get; }
```

## Exempel

Visar hur man arbetar med vissa områdesformat i en tabell.

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

// Skapa en anpassad tabellstil.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Villkorliga stilar är formateringsändringar som bara påverkar vissa av tabellens celler
// baserat på ett predikat, till exempel att cellerna är på den sista raden.
// Nedan följer tre sätt att komma åt en tabellstils villkorliga stilar från samlingen "ConditionalStyles".
// 1 - Efter stiltyp:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Enligt index:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Som en egenskap:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Använd utfyllnad och textformatering på villkorsstyrda stilar.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Lista alla möjliga stilvillkor.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Tillämpa den anpassade stilen, som innehåller alla villkorsstyrda stilar, på tabellen.
table.Style = tableStyle;

// Vår stil använder vissa villkorliga stilar som standard.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Vi måste aktivera alla andra stilar själva via egenskapen "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Se även

* class [BorderCollection](../../bordercollection/)
* class [ConditionalStyle](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
