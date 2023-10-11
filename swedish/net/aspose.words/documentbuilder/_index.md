---
title: Class DocumentBuilder
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.DocumentBuilder klass. Ger metoder för att infoga text bilder och annat innehåll specificera teckensnitt stycke och avsnittsformatering.
type: docs
weight: 450
url: /sv/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Ger metoder för att infoga text, bilder och annat innehåll, specificera teckensnitt, stycke och avsnittsformatering.

För att lära dig mer, besök[Översikt över dokumentbyggaren](https://docs.aspose.com/words/net/document-builder-overview/) dokumentationsartikel.

```csharp
public class DocumentBuilder
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Initierar en ny instans av den här klassen. |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Sant om teckensnittet är formaterat med fet stil. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Returnerar ett objekt som representerar aktuella tabellcellsformateringsegenskaper. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Hämtar noden som för närvarande är vald i denna DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Hämtar stycket som för närvarande är valt i detta`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Hämtar avsnittet som för närvarande är valt i detta`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Hämtar berättelsen som för närvarande är vald i denna`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Hämtar den strukturerade dokumenttaggen som för närvarande är vald i denna`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Hämtar eller ställer in[`Document`](./document/)objekt som detta objekt är kopplat till. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Returnerar ett objekt som representerar aktuella teckensnittsformateringsegenskaper. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Returnerar`Sann` om markören är i slutet av det aktuella stycket. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Returnerar **Sann** om markören är i slutet av en strukturerad dokumenttagg. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Returnerar`Sann` om markören är i början av det aktuella stycket (ingen text före markören). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Sant om teckensnittet är formaterat som kursivt. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Returnerar ett objekt som representerar aktuella listformateringsegenskaper. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Returnerar ett objekt som representerar aktuell siduppsättning och avsnittsegenskaper. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Returnerar ett objekt som representerar aktuella styckeformateringsegenskaper. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Returnerar ett objekt som representerar aktuella tabellradsformateringsegenskaper. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Hämtar/ställer in understrykningstyp för det aktuella teckensnittet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | Tar bort en rad från en tabell. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | Markerar den aktuella positionen i dokumentet som ett bokmärkesslut. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | Markerar den aktuella positionen i dokumentet som ett kolumnbokmärkesslut. Positionen måste vara i en tabellcell. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Markerar den aktuella positionen i dokumentet som ett redigerbart intervallslut. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | Markerar den aktuella positionen i dokumentet som ett redigerbart intervallslut. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Avslutar en tabellrad i dokumentet. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Avslutar en tabell i dokumentet. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | Infogar en brytning av angiven typ i dokumentet. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Infogar en tabellcell i dokumentet. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | Infogar ett kryssrutaformulär på den aktuella positionen. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | Infogar ett kryssrutaformulär på den aktuella positionen. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | Infogar ett formulärfält i kombinationsrutan på den aktuella positionen. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | Infogar ett dokument vid markörens position. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Infogar ett dokument vid markörens position. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(Document, ImportFormatMode, ImportFormatOptions) |  |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | Infogar ett Word-fält i ett dokument och uppdaterar fältresultatet. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | Infogar ett Word-fält i ett dokument och uppdaterar eventuellt fältresultatet. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | Infogar ett Word-fält i ett dokument utan att uppdatera fältresultatet. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | Infogar en fotnot eller slutnot i dokumentet. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | Infogar en fotnot eller slutnot i dokumentet. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Infogar en horisontell regelform i dokumentet. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | Infogar en HTML-sträng i dokumentet. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | Infogar en HTML-sträng i dokumentet. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | Infogar en HTML-sträng i dokumentet. Tillåter att ange ytterligare alternativ. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | Infogar en hyperlänk i dokumentet. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | Infogar en bild från en byte-array i dokumentet. Bilden infogas inline och i 100 % skala. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | Infogar en bild från ett .NETImage objekt i dokumentet. Bilden infogas inline och i 100 % skala. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | Infogar en bild från en ström i dokumentet. Bilden infogas inline och i 100 % skala. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | Infogar en bild från en fil eller URL i dokumentet. Bilden infogas inline och i 100 % skala. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | Infogar en inline-bild från en byte-array i dokumentet och skalar den till den angivna storleken. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | Infogar en inline-bild från ett .NETImage objekt i dokumentet och skalar det till den angivna storleken. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | Infogar en inline-bild från en ström i dokumentet och skalar den till den angivna storleken. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | Infogar en inline-bild från en fil eller URL i dokumentet och skalar den till den angivna storleken. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar en bild från en byte-array vid angiven position och storlek. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar en bild från ett .NETImage objekt vid angiven position och storlek. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar en bild från en ström vid angiven position och storlek. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar en bild från en fil eller URL på angiven position och storlek. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | Infogar en nod före markören. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | Infogar ett inbäddat OLE-objekt från en ström i dokumentet. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Upptäcker OLE-objekttyp med filtillägg. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Upptäcker OLE-objekttyp med hjälp av given progID-parameter. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | Infogar ett inbäddat OLE-objekt som ikon från en ström i dokumentet. Tillåter att ange ikonfil och bildtext. Upptäcker OLE-objekttyp med hjälp av given progID-parameter. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Upptäcker OLE-objekttyp med filtillägg. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Upptäcker OLE-objekttyp med hjälp av given progID-parameter. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar ett onlinevideoobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Infogar en styckebrytning i dokumentet. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | Infogar inline form med angiven typ och storlek. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Infogar fritt svävande form med angiven position, storlek och typ av textbrytning. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | Infogar en signaturrad vid den aktuella positionen. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Infogar en signaturrad vid den angivna positionen. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Infogar stilavgränsare i dokumentet. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | Infogar ett TOC-fält (innehållsförteckning) i dokumentet. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | Infogar ett textformulärfält på den aktuella positionen. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | Flyttar markören till en inline-nod eller till slutet av ett stycke. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | Flyttar markören till ett bokmärke. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | Flyttar markören till ett bokmärke med större precision. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | Flyttar markören till en tabellcell i det aktuella avsnittet. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Flyttar markören till slutet av dokumentet. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Flyttar markören till början av dokumentet. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | Flyttar markören till ett fält i dokumentet. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | Flyttar markören till början av en sidhuvud eller sidfot i det aktuella avsnittet. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | Flyttar markören till en position strax bortom det angivna kopplingsfältet och tar bort kopplingsfältet. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | Flyttar kopplingsfältet till det angivna kopplingsfältet. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | Flyttar markören till ett stycke i det aktuella avsnittet. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | Flyttar markören till början av brödtexten i ett angivet avsnitt. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(int, int) | Flyttar markören till en strukturerad dokumenttagg i det aktuella avsnittet. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(StructuredDocumentTag, int) | Flyttar markören till den strukturerade dokumenttaggen. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Hämtar teckenformatering som tidigare sparats i stacken. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Sparar aktuell teckenformatering i stacken. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | Markerar den aktuella positionen i dokumentet som en bokmärkesstart. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | Markerar den aktuella positionen i dokumentet som en kolumnbokmärkesstart. Positionen måste vara i en tabellcell. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Markerar den aktuella positionen i dokumentet som en redigerbar intervallstart. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Startar en tabell i dokumentet. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | Infogar en sträng i dokumentet vid den aktuella infogningspositionen. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Infogar en styckebrytning i dokumentet. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | Infogar en sträng och en styckebrytning i dokumentet. |

### Anmärkningar

`DocumentBuilder` gör processen att bygga en[`Document`](../document/) lättare. [`Document`](../document/) är ett sammansatt objekt som består av ett träd av noder och även om det är möjligt att infoga content noder direkt i trädet, kräver det god förståelse för trädstrukturen. `DocumentBuilder` är en "fasad" för den komplexa strukturen av[`Document`](../document/) och låter infoga innehåll och formatering snabbt och enkelt.

Skapa en`DocumentBuilder` och associera det med en[`Document`](../document/).

De`DocumentBuilder` har en intern markör där texten kommer att infogas när du ringer[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) och andra metoder. Du kan navigera i`DocumentBuilder` markören till en annan plats i ett dokument med hjälp av olika MoveToXXX-metoder.

Använd[`Font`](./font/)egenskap för att ange teckenformatering som kommer att gälla för all text som infogas från den aktuella positionen i dokumentet och framåt.

Använd[`ParagraphFormat`](./paragraphformat/) egenskap för att ange styckeformatering för aktuell och alla stycken som kommer att infogas.

Använd[`PageSetup`](./pagesetup/) egenskap för att ange sid- och avsnittsegenskaper för avsnittet current och alla avsnitt som kommer att infogas.

Använd[`CellFormat`](./cellformat/) och[`RowFormat`](./rowformat/) egenskaper för att specificera formateringsegenskaper för tabellceller och rader. Använder[`InsertCell`](./insertcell/) och [`EndRow`](./endrow/) metoder för att bygga en tabell.

Anteckna det[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) och[`PageSetup`](./pagesetup/) egenskaper uppdateras när du navigerar till en annan plats i dokumentet för att återspegla formateringsegenskaper som är tillgängliga på den nya platsen.

### Exempel

Visar hur man använder en dokumentbyggare för att skapa en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starta tabellen och fyll sedan i den första raden med två celler.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Anrop byggarens "EndRow"-metod för att starta en ny rad.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Visar hur du skapar sidhuvuden och sidfötter i ett dokument med DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange att vi vill ha olika sidhuvuden och sidfötter för första, jämna och udda sidor.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Skapa rubrikerna och lägg sedan till tre sidor i dokumentet för att visa varje rubriktyp.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Visar hur man bygger en tabell med anpassade ramar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Ställa in tabellformateringsalternativ för en dokumentbyggare
// kommer att tillämpa dem på varje rad och cell som vi lägger till med den.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Ändring av formateringen kommer att tillämpa den på den aktuella cellen,
// och eventuella nya celler som vi skapar med byggaren efteråt.
// Detta kommer inte att påverka cellerna som vi har lagt till tidigare.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Öka radhöjden så att den passar den vertikala texten.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


