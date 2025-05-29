---
title: ConditionalStyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: Upptäck metoden ConditionalStyleCollection GetEnumerator för att enkelt iterera igenom alla villkorsstyrda stilar och förbättra effektiviteten i din webbdesign.
type: docs
weight: 160
url: /sv/net/aspose.words/conditionalstylecollection/getenumerator/
---
## ConditionalStyleCollection.GetEnumerator method

Returnerar ett uppräknarobjekt som kan användas för att iterera över alla villkorliga stilar i samlingen.

```csharp
public IEnumerator<ConditionalStyle> GetEnumerator()
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

* class [ConditionalStyle](../../conditionalstyle/)
* class [ConditionalStyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
