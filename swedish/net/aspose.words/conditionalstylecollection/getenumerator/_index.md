---
title: ConditionalStyleCollection.GetEnumerator
second_title: Aspose.Words för .NET API Referens
description: ConditionalStyleCollection metod. Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla villkorliga stilar i samlingen.
type: docs
weight: 160
url: /sv/net/aspose.words/conditionalstylecollection/getenumerator/
---
## ConditionalStyleCollection.GetEnumerator method

Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla villkorliga stilar i samlingen.

```csharp
public IEnumerator<ConditionalStyle> GetEnumerator()
```

### Exempel

Visar hur man arbetar med vissa områdesstilar i en tabell.

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

// Villkorsstilar är formateringsändringar som bara påverkar vissa av tabellens celler
// baserat på ett predikat, som att cellerna är i den sista raden.
// Nedan finns tre sätt att komma åt en tabellstils villkorliga stilar från "ConditionalStyles"-samlingen.
// 1 - Efter stiltyp:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Efter index:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Som en egenskap:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Använd utfyllnad och textformatering på villkorliga stilar.
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

// Använd den anpassade stilen, som innehåller alla villkorliga stilar, på tabellen.
table.Style = tableStyle;

// Vår stil tillämpar vissa villkorade stilar som standard.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Vi kommer att behöva aktivera alla andra stilar själva via egenskapen "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Se även

* class [ConditionalStyle](../../conditionalstyle/)
* class [ConditionalStyleCollection](../)
* namnutrymme [Aspose.Words](../../conditionalstylecollection/)
* hopsättning [Aspose.Words](../../../)


