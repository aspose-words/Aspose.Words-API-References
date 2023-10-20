---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words per .NET
description: Aspose.Words.DocumentBuilder classe. Fornisce metodi per inserire testo immagini e altri contenuti specificare carattere formattazione di paragrafi e sezioni in C#.
type: docs
weight: 450
url: /it/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Fornisce metodi per inserire testo, immagini e altri contenuti, specificare carattere, formattazione di paragrafi e sezioni.

Per saperne di più, visita il[Panoramica del generatore di documenti](https://docs.aspose.com/words/net/document-builder-overview/) articolo di documentazione.

```csharp
public class DocumentBuilder
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Vero se il carattere è formattato in grassetto. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione della cella della tabella corrente. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Ottiene il nodo attualmente selezionato in questo DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Ottiene il paragrafo attualmente selezionato in this`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Ottiene la sezione attualmente selezionata in this`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Ottiene la storia attualmente selezionata in questo`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Ottiene il tag del documento strutturato attualmente selezionato in this`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Ottiene o imposta il file[`Document`](./document/)oggetto a cui è collegato questo oggetto. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione del carattere corrente. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Restituisce`VERO` se il cursore è alla fine del paragrafo corrente. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Restituisce**VERO** se il cursore è alla fine di un tag di documento strutturato. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Restituisce`VERO` se il cursore è all'inizio del paragrafo corrente (nessun testo prima del cursore). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Vero se il carattere è formattato come corsivo. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione dell'elenco corrente. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Restituisce un oggetto che rappresenta l'impostazione della pagina corrente e le proprietà della sezione. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione del paragrafo corrente. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione della riga della tabella corrente. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Ottiene/imposta il tipo di sottolineatura per il carattere corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | Elimina una riga da una tabella. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come fine segnalibro. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come fine segnalibro di colonna. La posizione deve essere in una cella della tabella. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Contrassegna la posizione corrente nel documento come fine dell'intervallo modificabile. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | Contrassegna la posizione corrente nel documento come fine dell'intervallo modificabile. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Termina una riga della tabella nel documento. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Termina una tabella nel documento. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | Inserisce un'interruzione del tipo specificato nel documento. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Inserisce una cella di tabella nel documento. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | Inserisce un campo modulo con casella di controllo nella posizione corrente. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | Inserisce un campo modulo con casella di controllo nella posizione corrente. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | Inserisce un campo modulo combobox nella posizione corrente. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | Inserisce un documento nella posizione del cursore. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Inserisce un documento nella posizione del cursore. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | Inserisce un campo Word in un documento e aggiorna il risultato del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Inserisce un campo Word in un documento e facoltativamente aggiorna il risultato del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | Inserisce un campo Word in un documento senza aggiornare il risultato del campo. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | Inserisce una nota a piè di pagina o di chiusura nel documento. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | Inserisce una nota a piè di pagina o di chiusura nel documento. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Inserisce una forma di filetto orizzontale nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | Inserisce una stringa HTML nel documento. Permette di specificare opzioni aggiuntive. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | Inserisce un collegamento ipertestuale nel documento. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | Inserisce un'immagine da un array di byte nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | Inserisce un'immagine da un .NETImage nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | Inserisce un'immagine da uno stream nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | Inserisce un'immagine da un file o un URL nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | Inserisce un'immagine in linea da un array di byte nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | Inserisce un'immagine in linea da un .NETImage nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | Inserisce un'immagine in linea da uno stream nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | Inserisce un'immagine in linea da un file o un URL nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da un array di byte nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da un .NETImageOggetto nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da uno stream nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da un file o da un URL nella posizione e dimensione specificate. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | Inserisce un nodo prima del cursore. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | Inserisce un oggetto OLE incorporato da uno stream nel documento. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE utilizzando l'estensione file. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | Inserisce un oggetto OLE incorporato come icona da uno stream nel documento. Permette di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Permette di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando l'estensione file. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Permette di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Inserisce un'interruzione di paragrafo nel documento. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | Inserisce una forma in linea con tipo e dimensione specificati. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce una forma mobile con posizione, dimensione e tipo di testo a capo specificati. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | Inserisce una riga per la firma nella posizione corrente. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce una riga della firma nella posizione specificata. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Inserisce il separatore di stile nel documento. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | Inserisce un campo TOC (tabella dei contenuti) nel documento. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | Inserisce un campo modulo di testo nella posizione corrente. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | Sposta il cursore su un nodo in linea o alla fine di un paragrafo. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | Sposta il cursore su un segnalibro. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | Sposta il cursore su un segnalibro con maggiore precisione. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | Sposta il cursore su una cella della tabella nella sezione corrente. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Sposta il cursore alla fine del documento. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Sposta il cursore all'inizio del documento. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | Sposta il cursore su un campo nel documento. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | Sposta il cursore all'inizio di un'intestazione o piè di pagina nella sezione corrente. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | Sposta il campo di unione nel campo di unione specificato. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | Sposta il cursore su un paragrafo della sezione corrente. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | Sposta il cursore all'inizio del corpo in una sezione specificata. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | Sposta il cursore su un tag di documento strutturato nella sezione corrente. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | Sposta il cursore sul tag del documento strutturato. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Recupera la formattazione dei caratteri precedentemente salvata nello stack. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Salva la formattazione corrente del carattere nello stack. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come inizio segnalibro. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come inizio di un segnalibro di colonna. La posizione deve essere in una cella della tabella. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Contrassegna la posizione corrente nel documento come inizio di un intervallo modificabile. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Avvia una tabella nel documento. |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | Inserisce una stringa nel documento nella posizione di inserimento corrente. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Inserisce un'interruzione di paragrafo nel documento. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | Inserisce una stringa e un'interruzione di paragrafo nel documento. |

## Osservazioni

`DocumentBuilder` rende il processo di costruzione a[`Document`](../document/) più facile. [`Document`](../document/) è un oggetto composito costituito da un albero di nodi e sebbene sia possibile inserire content nodes direttamente nell'albero, richiede una buona conoscenza della struttura ad albero. `DocumentBuilder` è una "facciata" per la complessa struttura dell'[`Document`](../document/) e consente di inserire contenuti e formattazioni in modo rapido e semplice.

Creare un`DocumentBuilder` e associarlo ad a[`Document`](../document/).

IL`DocumentBuilder` ha un cursore interno in cui verrà inserito il testo quando chiami[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) e altri metodi. Puoi navigare nel`DocumentBuilder` cursore in una posizione diversa in un documento utilizzando vari metodi MoveToXXX.

Usa il[`Font`](./font/)proprietà per specificare la formattazione dei caratteri che verrà applicata a tutto il testo inserito dalla posizione corrente nel documento in poi.

Usa il[`ParagraphFormat`](./paragraphformat/) proprietà per specificare la formattazione del paragrafo per current e tutti i paragrafi che verranno inseriti.

Usa il[`PageSetup`](./pagesetup/) property per specificare le proprietà della pagina e della sezione per la sezione current e tutte le sezioni che verranno inserite.

Usa il[`CellFormat`](./cellformat/) E[`RowFormat`](./rowformat/) proprietà per specificare le proprietà di formattazione per le celle e le righe della tabella. Utente il[`InsertCell`](./insertcell/) e [`EndRow`](./endrow/) metodi per costruire una tabella

Notare che[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) E[`PageSetup`](./pagesetup/) le proprietà vengono aggiornate ogni volta che ti sposti in una posizione diversa nel documento per riflettere le proprietà di formattazione disponibili nella nuova posizione.

## Esempi

Mostra come utilizzare un generatore di documenti per creare una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inizia la tabella, quindi compila la prima riga con due celle.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Chiama il metodo "EndRow" del builder per iniziare una nuova riga.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Mostra come creare intestazioni e piè di pagina in un documento utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica che vogliamo intestazioni e piè di pagina diversi per le prime pagine, pari e dispari.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crea le intestazioni, quindi aggiungi tre pagine al documento per visualizzare ciascun tipo di intestazione.
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

Mostra come creare una tabella con bordi personalizzati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Impostazione delle opzioni di formattazione della tabella per un generatore di documenti
// li applicherà a ogni riga e cella che aggiungiamo con esso.
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

// La modifica della formattazione la applicherà alla cella corrente,
// e tutte le nuove celle che creeremo successivamente con il builder.
// Ciò non influenzerà le celle che abbiamo aggiunto in precedenza.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Aumenta l'altezza della riga per adattarla al testo verticale.
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

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
