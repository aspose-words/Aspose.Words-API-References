---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.DocumentBuilder la soluzione per inserire senza sforzo testo, immagini ed elementi di formattazione nei documenti.
type: docs
weight: 660
url: /it/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Fornisce metodi per inserire testo, immagini e altri contenuti, specificare il font, la formattazione di paragrafi e sezioni.

Per saperne di più, visita il[Panoramica di Document Builder](https://docs.aspose.com/words/net/document-builder-overview/) articolo di documentazione.

```csharp
public class DocumentBuilder
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](documentbuilder/#constructor_3)(*[DocumentBuilderOptions](../documentbuilderoptions/)*) | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](documentbuilder/#constructor_2)(*[Document](../document/), [DocumentBuilderOptions](../documentbuilderoptions/)*) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Vero se il font è formattato in grassetto. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione delle celle della tabella corrente. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Ottiene il nodo attualmente selezionato in questo DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Ottiene il paragrafo attualmente selezionato in questo`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Ottiene la sezione attualmente selezionata in questo`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Ottiene la storia attualmente selezionata in questo`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Ottiene il tag del documento strutturato attualmente selezionato in questo`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Ottiene o imposta il[`Document`](./document/) oggetto a cui è collegato questo oggetto. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione del carattere corrente. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Restituisce`VERO` se il cursore si trova alla fine del paragrafo corrente. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Restituisce**VERO** se il cursore si trova alla fine di un tag di documento strutturato. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Restituisce`VERO`se il cursore si trova all'inizio del paragrafo corrente (nessun testo prima del cursore). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Vero se il font è formattato in corsivo. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione dell'elenco corrente. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Restituisce un oggetto che rappresenta l'impostazione di pagina corrente e le proprietà della sezione. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione del paragrafo corrente. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Restituisce un oggetto che rappresenta le proprietà di formattazione delle righe della tabella corrente. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Ottiene/imposta il tipo di sottolineatura per il font corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | Elimina una riga da una tabella. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come fine segnalibro. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come fine segnalibro di colonna. La posizione deve essere in una cella della tabella. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Termina una riga della tabella nel documento. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Termina una tabella nel documento. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | Inserisce un'interruzione del tipo specificato nel documento. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Inserisce una cella della tabella nel documento. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_2)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_3)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/), [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | Inserisce un campo modulo casella di controllo nella posizione corrente. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | Inserisce un campo modulo casella di controllo nella posizione corrente. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | Inserisce un campo modulo combobox nella posizione corrente. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | Inserisce un documento nella posizione del cursore. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Inserisce un documento nella posizione del cursore. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Inserisce un documento in linea nella posizione del cursore. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | Inserisce un campo Word in un documento e aggiorna il risultato del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Inserisce un campo Word in un documento e, facoltativamente, aggiorna il risultato del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | Inserisce un campo Word in un documento senza aggiornare il risultato del campo. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | Inserisce una nota a piè di pagina o una nota di chiusura nel documento. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | Inserisce una nota a piè di pagina o una nota di chiusura nel documento. |
| [InsertForms2OleControl](../../aspose.words/documentbuilder/insertforms2olecontrol/)(*[Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)*) | Inserimenti[`Forms2OleControl`](../../aspose.words.drawing.ole/forms2olecontrol/) oggetto nella posizione corrente. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape)(*params ShapeBase[]*) | Raggruppa le forme passate come parametro in un nuovo nodo GroupShape che viene inserito nella posizione corrente. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape_1)(*double, double, double, double, params ShapeBase[]*) | Raggruppa le forme passate come parametro in un nuovo nodo GroupShape della dimensione specificata che viene inserito nella posizione specificata. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Inserisce una forma di regola orizzontale nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | Inserisce una stringa HTML nel documento. Permette di specificare opzioni aggiuntive. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | Inserisce un collegamento ipertestuale nel documento. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | Inserisce un'immagine da un array di byte nel documento. L'immagine viene inserita in linea e in scala al 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | Inserisce un'immagine da un file .NETImage Oggetto nel documento. L'immagine viene inserita in linea e in scala al 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | Inserisce un'immagine da un flusso nel documento. L'immagine viene inserita in linea e in scala al 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | Inserisce un'immagine da un file o da un URL nel documento. L'immagine viene inserita in linea e in scala al 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | Inserisce un'immagine in linea da un array di byte nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | Inserisce un'immagine in linea da un file .NETImage oggetto nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | Inserisce un'immagine in linea da un flusso nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | Inserisce un'immagine in linea da un file o URL nel documento e la ridimensiona alla dimensione specificata. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da un array di byte nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da un file .NETImage oggetto nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da un flusso nella posizione e dimensione specificate. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un'immagine da un file o URL nella posizione e dimensione specificate. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | Inserisce un nodo prima del cursore. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | Inserisce un oggetto OLE incorporato da un flusso nel documento. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE tramite l'estensione del file. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | Inserisce un oggetto OLE incorporato come icona da un flusso nel documento. Consente di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE tramite l'estensione del file. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Inserisce un'interruzione di paragrafo nel documento. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | Inserisce una forma in linea con il tipo e le dimensioni specificati. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce una forma mobile con posizione, dimensione e tipo di avvolgimento del testo specificati. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | Inserisce una riga di firma nella posizione corrente. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserisce una riga di firma nella posizione specificata. |
| [InsertStructuredDocumentTag](../../aspose.words/documentbuilder/insertstructureddocumenttag/)(*[SdtType](../../aspose.words.markup/sdttype/)*) | Inserisce un[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) nel documento. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Inserisce un separatore di stile nel documento. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | Inserisce un campo TOC (indice) nel documento. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | Inserisce un campo modulo di testo nella posizione corrente. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | Sposta il cursore su un nodo in linea o alla fine di un paragrafo. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | Sposta il cursore su un segnalibro. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | Sposta il cursore su un segnalibro con maggiore precisione. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | Sposta il cursore su una cella della tabella nella sezione corrente. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Sposta il cursore alla fine del documento. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Sposta il cursore all'inizio del documento. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | Sposta il cursore su un campo nel documento. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | Sposta il cursore all'inizio di un'intestazione o di un piè di pagina nella sezione corrente. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | Sposta il campo di unione nel campo di unione specificato. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | Sposta il cursore su un paragrafo nella sezione corrente. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | Sposta il cursore all'inizio del corpo in una sezione specificata. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | Sposta il cursore su un tag di documento strutturato nella sezione corrente. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | Sposta il cursore sul tag del documento strutturato. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Recupera la formattazione dei caratteri precedentemente salvata nello stack. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Salva la formattazione corrente del carattere nello stack. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come inizio del segnalibro. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | Contrassegna la posizione corrente nel documento come inizio di un segnalibro di colonna. La posizione deve essere in una cella della tabella. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Contrassegna la posizione corrente nel documento come inizio di un intervallo modificabile. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Avvia una tabella nel documento. |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | Inserisce una stringa nel documento nella posizione di inserimento corrente. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Inserisce un'interruzione di paragrafo nel documento. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | Inserisce una stringa e un'interruzione di paragrafo nel documento. |

## Osservazioni

`DocumentBuilder` rende il processo di costruzione di un[`Document`](../document/) più facile. [`Document`](../document/) è un oggetto composito costituito da un albero di nodi e, sebbene sia possibile inserire nodi content direttamente nell'albero, è richiesta una buona comprensione della struttura dell'albero. `DocumentBuilder` è una "facciata" per la complessa struttura di[`Document`](../document/) e consente a di inserire contenuti e formattazione in modo rapido e semplice.

Crea un`DocumentBuilder` e associarlo ad un[`Document`](../document/).

IL`DocumentBuilder` ha un cursore interno dove verrà inserito il testo quando si chiama[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) e altri metodi. Puoi navigare nel`DocumentBuilder` cursore in una posizione diversa in un documento utilizzando vari metodi MoveToXXX.

Utilizzare il[`Font`](./font/) proprietà per specificare la formattazione dei caratteri che verrà applicata a tutto il testo inserito dalla posizione corrente nel documento in poi.

Utilizzare il[`ParagraphFormat`](./paragraphformat/) proprietà per specificare la formattazione del paragrafo current e di tutti i paragrafi che verranno inseriti.

Utilizzare il[`PageSetup`](./pagesetup/) proprietà per specificare le proprietà di pagina e sezione per la sezione current e tutte le sezioni che verranno inserite.

Utilizzare il[`CellFormat`](./cellformat/) E[`RowFormat`](./rowformat/) proprietà per specificare le proprietà di formattazione per le celle e le righe della tabella. Utilizzare l'[`InsertCell`](./insertcell/) e [`EndRow`](./endrow/) metodi per costruire una tabella.

Notare che[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) E[`PageSetup`](./pagesetup/) le proprietà vengono aggiornate ogni volta che si passa a un punto diverso del documento per riflettere le proprietà di formattazione disponibili nella nuova posizione.

## Esempi

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

// Specificare che si vogliono intestazioni e piè di pagina diversi per la prima pagina, le pagine pari e quelle dispari.
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
// li applicheremo a ogni riga e cella che aggiungeremo.
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

// La modifica della formattazione verrà applicata alla cella corrente,
// e tutte le nuove celle che creeremo in seguito con il builder.
// Ciò non influirà sulle celle aggiunte in precedenza.
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
