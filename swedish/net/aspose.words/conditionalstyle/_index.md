---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words för .NET
description: Aspose.Words.ConditionalStyle klass. Representerar speciell formatering som tillämpas på någon del av en tabell med tilldelad tabellstil i C#.
type: docs
weight: 310
url: /sv/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Representerar speciell formatering som tillämpas på någon del av en tabell med tilldelad tabellstil.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public sealed class ConditionalStyle
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Hämtar samlingen av standardcellkanter för den villkorliga stilen. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till under innehållet i tabellceller. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Hämtar teckenformateringen för den villkorliga stilen. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till till vänster om innehållet i tabellceller. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Hämtar styckeformateringen av den villkorliga stilen. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till till höger om innehållet i tabellceller. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Får en[`Shading`](../shading/) objekt som refererar till skuggningsformateringen för denna villkorliga stil. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till ovanför innehållet i tabellceller. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Hämtar tabellområde som denna villkorliga stil relaterar till. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Rensar formateringen av denna villkorliga stil. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | Jämför denna villkorliga stil med det angivna objektet. |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Beräknar hashkod för detta objekt. |

## Exempel

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
