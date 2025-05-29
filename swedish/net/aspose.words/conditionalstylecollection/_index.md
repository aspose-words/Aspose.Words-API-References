---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.ConditionalStyleCollection-klassen för att hantera ConditionalStyle-objekt effektivt, vilket förbättrar dokumentformatering och anpassning.
type: docs
weight: 520
url: /sv/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Representerar en samling av[`ConditionalStyle`](../conditionalstyle/) objekt.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Hämtar cellformatet längst ner till vänster. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Hämtar cellstilen längst ner till höger. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Hämtar antalet villkorsstyrda stilar i samlingen. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Hämtar jämn kolumnränder. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Hämtar bandningsstilen för jämna rader. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Hämtar den första kolumnstilen. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Hämtar stilen för första raden. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Hämtar en[`ConditionalStyle`](../conditionalstyle/) objekt efter villkorlig stiltyp. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Hämtar den sista kolumnstilen. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Hämtar stilen för den sista raden. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Hämtar den udda kolumnbandningsstilen. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Hämtar stilen för udda rader. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Hämtar cellformatet längst upp till vänster. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Hämtar cellformatet överst till höger. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Rensar alla villkorsstyrda format i tabellformatet. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla villkorliga stilar i samlingen. |

## Anmärkningar

Det går inte att lägga till eller ta bort objekt från den här samlingen. Den innehåller en permanent uppsättning objekt: ett objekt för varje värde av[`ConditionalStyleType`](../conditionalstyletype/) uppräkningstyp.

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

* class [ConditionalStyle](../conditionalstyle/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
