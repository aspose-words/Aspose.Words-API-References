---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ConditionalStyleType-enum för att definiera dynamisk tabellformatering. Förbättra dina dokumentformat med flexibla, villkorliga alternativ!
type: docs
weight: 530
url: /sv/net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

Representerar möjliga tabellområden för vilka villkorsstyrd formatering kan definieras i en tabellstil.

```csharp
public enum ConditionalStyleType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| FirstRow | `0` | Anger formateringen av den första raden i en tabell. |
| FirstColumn | `1` | Anger formateringen av den första kolumnen i en tabell. |
| LastRow | `2` | Anger formateringen av den sista raden i en tabell. |
| LastColumn | `3` | Anger formateringen av den sista kolumnen i en tabell. |
| OddRowBanding | `4` | Anger formatering av udda radremsa. |
| OddColumnBanding | `5` | Anger formatering av udda kolumnremsa. |
| EvenRowBanding | `6` | Anger formatering av radremsa med jämna numreringar. |
| EvenColumnBanding | `7` | Anger formatering av jämnt numrerade kolumnremsor. |
| TopLeftCell | `8` | Anger formateringen av den övre vänstra cellen i en tabell. |
| TopRightCell | `9` | Anger formateringen av den övre högra cellen i en tabell. |
| BottomLeftCell | `10` | Anger formateringen av den nedre vänstra cellen i en tabell. |
| BottomRightCell | `11` | Anger formateringen av den nedre högra cellen i en tabell. |

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
