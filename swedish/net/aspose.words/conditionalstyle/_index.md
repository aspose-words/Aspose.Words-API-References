---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ConditionalStyle för avancerad tabellformatering. Förbättra dina dokument med dynamiska stilar och förbättra läsbarheten utan ansträngning.
type: docs
weight: 510
url: /sv/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Representerar specialformatering som tillämpats på ett område i en tabell med tilldelad tabellstil.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public sealed class ConditionalStyle
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Hämtar samlingen av standardcellkantlinjer för den villkorliga stilen. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till under innehållet i tabellceller. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Hämtar teckenformateringen för den villkorliga stilen. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till vänster om innehållet i tabellceller. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Hämtar styckeformateringen för den villkorsstyrda stilen. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till till höger om innehållet i tabellceller. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Får en[`Shading`](../shading/) objekt som refererar till skuggningsformateringen för denna villkorsstyrda stil. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till ovanför innehållet i tabellceller. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Hämtar tabellområdet som denna villkorsstyrda stil relaterar till. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Rensar formateringen av denna villkorsstyrda stil. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | Jämför denna villkorsstyrda stil med det angivna objektet. |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Beräknar hashkod för detta objekt. |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
