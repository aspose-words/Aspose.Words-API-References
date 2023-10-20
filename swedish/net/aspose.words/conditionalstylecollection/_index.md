---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words för .NET
description: Aspose.Words.ConditionalStyleCollection klass. Representerar en samling avConditionalStyle objekt i C#.
type: docs
weight: 320
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
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Får cellstilen längst ner till höger. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Hämtar antalet villkorade stilar i samlingen. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Får den jämna kolumnbandsstilen. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Får den jämna radbandsstilen. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Hämtar den första kolumnstilen. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Får den första radens stil. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Hämtar en[`ConditionalStyle`](../conditionalstyle/) objekt efter villkorlig stiltyp. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Hämtar den sista kolumnstilen. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Hämtar den sista radens stil. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Får den udda kolumnbandsstilen. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Får den udda radbandsstilen. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Får den övre vänstra cellstilen. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Får den övre högra cellstilen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Rensar alla villkorliga stilar i tabellstilen. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla villkorliga stilar i samlingen. |

## Anmärkningar

Det är inte möjligt att lägga till eller ta bort objekt från den här samlingen. Den innehåller permanent uppsättning objekt: ett objekt för varje värde av[`ConditionalStyleType`](../conditionalstyletype/) uppräkningstyp.

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

* class [ConditionalStyle](../conditionalstyle/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
