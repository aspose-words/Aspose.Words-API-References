---
title: TableStyle
second_title: Aspose.Words för .NET API Referens
description: Representerar en tabellstil.
type: docs
weight: 5920
url: /sv/net/aspose.words/tablestyle/
---
## TableStyle class

Representerar en tabellstil.

```csharp
public class TableStyle : Style
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Får alla alias för denna stil. Om stilen inte har några alias returneras tom array av sträng. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Anger justeringen för tabellstilen. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Hämtar eller ställer in en flagga som anger om text i en tabellrad tillåts delas över en sidbrytning. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Hämtar/ställer in namnet på stilen som denna stil är baserad på. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Hämtar eller ställer in om detta är en stil för en höger-till-vänster-tabell. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Hämtar samlingen av standardcellkanter för stilen. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till under innehållet i tabellceller. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Sant om denna stil är en av de inbyggda stilarna i MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) mellan cellerna. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Hämtar eller ställer in ett antal kolumner som ska inkluderas i bandningen när stilen anger udda/jämna kolumner. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Samling av villkorliga stilar som kan definieras för denna tabellstil. |
| [Document](../../aspose.words/style/document/) { get; } | Hämtar ägardokumentet. |
| [Font](../../aspose.words/style/font/) { get; } | Hämtar teckenformateringen för stilen. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Sant när stilen är en av de inbyggda rubrikstilarna. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Anger om denna stil visas i Quick Style-galleriet i MS Word UI. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Hämtar eller ställer in värdet som representerar vänster indrag i en tabell. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till till vänster om innehållet i tabellceller. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Hämtar namnet på stilen som är länkad till denna. Returnerar tom sträng om inga stilar är länkade. |
| [List](../../aspose.words/style/list/) { get; } | Hämtar listan som definierar formateringen av denna liststil. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Ger tillgång till listformateringsegenskaperna för en styckestil. |
| [Name](../../aspose.words/style/name/) { get; set; } | Hämtar eller ställer in namnet på stilen. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Hämtar/ställer in namnet på formatet som ska tillämpas automatiskt på ett nytt stycke som infogas efter a stycke formaterat med det angivna formatet. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Hämtar formatets styckeformatering. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till till höger om innehållet i tabellceller. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Hämtar eller ställer in ett antal rader som ska inkluderas i bandningen när stilen anger udda/jämna radband. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | Får en[`Shading`](../shading/) objekt som hänvisar till skuggningsformateringen för tabellceller. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Hämtar den lokala stilidentifieraren för en inbyggd stil. |
| [Styles](../../aspose.words/style/styles/) { get; } | Får samlingen av stilar som denna stil tillhör. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till ovanför innehållet i tabellceller. |
| [Type](../../aspose.words/style/type/) { get; } | Hämtar stiltypen (stycke eller tecken). |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Anger den vertikala justeringen för cellerna. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(Style) | Jämförs med den angivna stilen. Stilar Istds jämförs endast för inbyggda stilar. Formatmallars standarder ingår inte i jämförelsen. Basstil, länkad stil och nästa styckestil jämförs rekursivt. |
| [Remove](../../aspose.words/style/remove/)() | Tar bort den angivna stilen från dokumentet. |

### Exempel

Visar hur man skapar anpassade stilinställningar för tabellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Att ställa in stilegenskaperna för en tabell kan påverka egenskaperna för själva tabellen.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Se även

* class [Style](../style/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
