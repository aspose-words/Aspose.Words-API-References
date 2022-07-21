---
title: DocumentBuilder
second_title: Aspose.Words per .NET API Reference
description: Fornisce metodi per inserire testo immagini e altro contenuto specificare font paragrafo e formattazione della sezione.
type: docs
weight: 440
url: /it/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Fornisce metodi per inserire testo, immagini e altro contenuto, specificare font, paragrafo e formattazione della sezione.

```csharp
public class DocumentBuilder
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DocumentBuilder](documentbuilder#constructor)() | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](documentbuilder#constructor_1)(Document) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold) { get; set; } | Vero se il carattere è formattato in grassetto. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione della cella della tabella correnti. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode) { get; } | Ottiene il nodo attualmente selezionato in questo DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph) { get; } | Ottiene il paragrafo attualmente selezionato in questo DocumentBuilder. |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection) { get; } | Ottiene la sezione attualmente selezionata in questo DocumentBuilder. |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory) { get; } | Ottiene la storia attualmente selezionata in questo DocumentBuilder. |
| [Document](../../aspose.words/documentbuilder/document) { get; set; } | Ottiene o imposta il[`Document`](./document) oggetto a cui questo oggetto è collegato. |
| [Font](../../aspose.words/documentbuilder/font) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione del carattere correnti. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph) { get; } | Restituisce vero se il cursore si trova alla fine del paragrafo corrente. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph) { get; } | Restituisce vero se il cursore si trova all'inizio del paragrafo corrente (nessun testo prima del cursore). |
| [Italic](../../aspose.words/documentbuilder/italic) { get; set; } | Vero se il carattere è formattato in corsivo. |
| [ListFormat](../../aspose.words/documentbuilder/listformat) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione dell'elenco corrente. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup) { get; } | Restituisce un oggetto che rappresenta l'impostazione di pagina corrente e le proprietà della sezione. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione del paragrafo corrente. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione della riga della tabella corrente. |
| [Underline](../../aspose.words/documentbuilder/underline) { get; set; } | Ottiene/imposta il tipo di sottolineatura per il font corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow)(int, int) | Elimina una riga da una tabella. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark)(string) | Contrassegna la posizione corrente nel documento come fine segnalibro. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark)(string) | Contrassegna la posizione corrente nel documento come fine di un segnalibro di colonna. La posizione deve essere in una cella di tabella. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange#endeditablerange)() | Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange#endeditablerange_1)(EditableRangeStart) | Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile. |
| [EndRow](../../aspose.words/documentbuilder/endrow)() | Termina una riga della tabella nel documento. |
| [EndTable](../../aspose.words/documentbuilder/endtable)() | Termina una tabella nel documento. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak)(BreakType) | Inserisce un'interruzione del tipo specificato nel documento. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell)() | Inserisce una cella di tabella nel documento. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart#insertchart_1)(ChartType, double, double) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox#insertcheckbox_1)(string, bool, int) | Inserisce un campo modulo checkbox nella posizione corrente. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox#insertcheckbox)(string, bool, bool, int) | Inserisce un campo modulo checkbox nella posizione corrente. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox)(string, string[], int) | Inserisce un campo modulo casella combinata nella posizione corrente. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument#insertdocument)(Document, ImportFormatMode) | Inserisce un documento nella posizione del cursore. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Inserisce un documento nella posizione del cursore. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield_1)(string) | Inserisce un campo Word in un documento e aggiorna il risultato del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield)(FieldType, bool) | Inserisce un campo Word in un documento e facoltativamente aggiorna il risultato del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield#insertfield_2)(string, string) | Inserisce un campo Word in un documento senza aggiornare il risultato del campo. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote#insertfootnote)(FootnoteType, string) | Inserisce una nota a piè di pagina o una nota di chiusura nel documento. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote#insertfootnote_1)(FootnoteType, string, string) | Inserisce una nota a piè di pagina o una nota di chiusura nel documento. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule)() | Inserisce una forma a righello orizzontale nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml)(string) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml_2)(string, bool) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml#inserthtml_1)(string, HtmlInsertOptions) | Inserisce una stringa HTML nel documento. Consente di specificare opzioni aggiuntive. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink)(string, string, bool) | Inserisce un collegamento ipertestuale nel documento. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage)(byte[]) | Inserisce un'immagine da un array di byte nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_3)(Image) | Inserisce un'immagine da un .NETImage oggetto nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_6)(Stream) | Inserisce un'immagine da uno stream nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_9)(string) | Inserisce un'immagine da un file o da un URL nel documento. L'immagine viene inserita in linea e in scala 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_2)(byte[], double, double) | Inserisce un'immagine inline da una matrice di byte nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_5)(Image, double, double) | Inserisce un'immagine inline da un .NETImage nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_8)(Stream, double, double) | Inserisce un'immagine in linea da un flusso nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_11)(string, double, double) | Inserisce un'immagine in linea da un file o un URL nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce un'immagine da un array di byte nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce un'immagine da un .NETImage oggetto nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce un'immagine da uno stream nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce un'immagine da un file o un URL nella posizione e dimensione specificate. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode)(Node) | Inserisce un nodo a livello di testo all'interno del paragrafo corrente prima del cursore. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject)(Stream, string, bool, Stream) | Inserisce un oggetto OLE incorporato da un flusso nel documento. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject_1)(string, bool, bool, Stream) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE utilizzando l'estensione del file. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject#insertoleobject_2)(string, string, bool, bool, Stream) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon)(Stream, string, string, string) | Inserisce un oggetto OLE incorporato come icona da uno stream nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon_1)(string, bool, string, string) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando l'estensione del file. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon#insertoleobjectasicon_2)(string, string, bool, string, string) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_1)(string, double, double) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_3)(string, string, byte[], double, double) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph)() | Inserisce un'interruzione di paragrafo nel documento. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape#insertshape_1)(ShapeType, double, double) | Inserisce la forma in linea con il tipo e la dimensione specificati. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserisce una forma fluttuante con posizione, dimensione e tipo di avvolgimento del testo specificati. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline#insertsignatureline)(SignatureLineOptions) | Inserisce una linea di firma nella posizione corrente. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Inserisce una riga della firma nella posizione specificata. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator)() | Inserisce il separatore di stile nel documento. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents)(string) | Inserisce un campo TOC (indice) nel documento. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput)(string, TextFormFieldType, string, string, int) | Inserisce un campo modulo di testo nella posizione corrente. |
| [MoveTo](../../aspose.words/documentbuilder/moveto)(Node) | Sposta il cursore su un nodo in linea o alla fine di un paragrafo. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark#movetobookmark)(string) | Sposta il cursore su un segnalibro. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark#movetobookmark_1)(string, bool, bool) | Sposta il cursore su un segnalibro con maggiore precisione. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell)(int, int, int, int) | Sposta il cursore su una cella della tabella nella sezione corrente. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend)() | Sposta il cursore alla fine del documento. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart)() | Sposta il cursore all'inizio del documento. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield)(Field, bool) | Sposta il cursore su un campo del documento. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter)(HeaderFooterType) | Sposta il cursore all'inizio di un'intestazione o un piè di pagina nella sezione corrente. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield#movetomergefield)(string) | Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield#movetomergefield_1)(string, bool, bool) | Sposta il campo di unione nel campo di unione specificato. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph)(int, int) | Sposta il cursore su un paragrafo nella sezione corrente. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection)(int) | Sposta il cursore all'inizio del corpo in una sezione specificata. |
| [PopFont](../../aspose.words/documentbuilder/popfont)() | Recupera la formattazione dei caratteri precedentemente salvata nello stack. |
| [PushFont](../../aspose.words/documentbuilder/pushfont)() | Salva la formattazione del carattere corrente nello stack. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark)(string) | Contrassegna la posizione corrente nel documento come inizio segnalibro. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark)(string) | Contrassegna la posizione corrente nel documento come inizio di un segnalibro di colonna. La posizione deve essere in una cella di tabella. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange)() | Contrassegna la posizione corrente nel documento come inizio intervallo modificabile. |
| [StartTable](../../aspose.words/documentbuilder/starttable)() | Avvia una tabella nel documento. |
| [Write](../../aspose.words/documentbuilder/write)(string) | Inserisce una stringa nel documento nella posizione di inserimento corrente. |
| [Writeln](../../aspose.words/documentbuilder/writeln#writeln)() | Inserisce un'interruzione di paragrafo nel documento. |
| [Writeln](../../aspose.words/documentbuilder/writeln#writeln_1)(string) | Inserisce una stringa e un'interruzione di paragrafo nel documento. |

### Osservazioni

**Costruttore di documenti** rende il processo di costruzione a **Documento** più facile.  **Documento**è un oggetto composto costituito da un albero di nodi e sebbene sia possibile inserire i nodi content direttamente nell'albero, richiede una buona comprensione della struttura ad albero.  **Costruttore di documenti** è una "facciata" per la complessa struttura di **Documento** e permette di inserire contenuto e formattazione in modo rapido e semplice.

Creare un **Costruttore di documenti** e associarlo ad a[`Document`](./document).

Il **Costruttore di documenti** ha un cursore interno dove verrà inserito il testo quando chiami[`Write`](./write) ,[`Writeln`](./writeln) ,[`InsertBreak`](./insertbreak) e altri metodi. Puoi navigare nel **Costruttore di documenti** cursore in una posizione diversa in un documento utilizzando vari metodi MoveToXXX.

Utilizzare il[`Font`](./font) per specificare la formattazione dei caratteri che si applicherà a tutto il testo inserito dalla posizione corrente nel documento in poi.

Utilizzare il[`ParagraphFormat`](./paragraphformat) per specificare la formattazione del paragrafo per l'oggetto corrente e tutti i paragrafi che verranno inseriti.

Utilizzare il[`PageSetup`](./pagesetup)per specificare le proprietà della pagina e della sezione per la sezione corrente e per tutte le sezioni che verranno inserite.

Utilizzare il[`CellFormat`](./cellformat) e[`RowFormat`](./rowformat) proprietà per specificare le proprietà di formattazione per le celle e le righe della tabella. Utente il[`InsertCell`](./insertcell) e [`EndRow`](./endrow) metodi per costruire una tabella.

Notare che **Font** , **Formato paragrafo** e **Impostazione della pagina** le proprietà vengono aggiornate ogni volta che ci si sposta in una posizione diversa nel documento per riflettere le proprietà di formattazione disponibili nella nuova posizione.

### Esempi

Mostra come utilizzare un generatore di documenti per creare una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Avvia la tabella, quindi popola la prima riga con due celle.
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

// Specifica che vogliamo intestazioni e piè di pagina diversi per le prime, pari e dispari.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crea le intestazioni, quindi aggiungi tre pagine al documento per visualizzare ogni tipo di intestazione.
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
// e tutte le nuove celle che creiamo con il builder in seguito.
// Ciò non influirà sulle celle che abbiamo aggiunto in precedenza.
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

* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
