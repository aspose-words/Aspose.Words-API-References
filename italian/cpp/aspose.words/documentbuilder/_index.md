---
title: "Aspose::Words::DocumentBuilder class"
linktitle: "DocumentBuilder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder class. Fornisce metodi per inserire testo, immagini e altri contenuti, specificare la formattazione di carattere, paragrafo e sezione. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


Fornisce metodi per inserire testo, immagini e altri contenuti, specificare il carattere, la formattazione di paragrafi e sezioni. Per saperne di più, visita l'articolo di documentazione [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/).

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | Elimina una riga da una tabella. |
| [DocumentBuilder](./documentbuilder/)() | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Inizializza una nuova istanza di questa classe. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Inizializza una nuova istanza di questa classe. |
| [EndBookmark](./endbookmark/)(const System::String\&) | Segna la posizione corrente nel documento come fine segnalibro. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | Segna la posizione corrente nel documento come fine segnalibro di colonna. La posizione deve trovarsi in una cella di tabella. |
| [EndEditableRange](./endeditablerange/)() | Segna la posizione corrente nel documento come fine intervallo modificabile. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | Segna la posizione corrente nel documento come fine intervallo modificabile. |
| [EndRow](./endrow/)() | Termina una riga di tabella nel documento. |
| [EndTable](./endtable/)() | Termina una tabella nel documento. |
| [get_Bold](./get_bold/)() | Vero se il carattere è formattato in grassetto. |
| [get_CellFormat](./get_cellformat/)() | Restituisce un oggetto che rappresenta le proprietà di formattazione della cella di tabella corrente. |
| [get_CurrentNode](./get_currentnode/)() | Ottiene il nodo attualmente selezionato in questo [DocumentBuilder](./). |
| [get_CurrentParagraph](./get_currentparagraph/)() | Ottiene il paragrafo attualmente selezionato in questo [DocumentBuilder](./). |
| [get_CurrentSection](./get_currentsection/)() | Ottiene la sezione attualmente selezionata in questo [DocumentBuilder](./). |
| [get_CurrentStory](./get_currentstory/)() | Ottiene la storia attualmente selezionata in questo [DocumentBuilder](./). |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | Ottiene il tag di documento strutturato attualmente selezionato in questo [DocumentBuilder](./). |
| [get_Document](./get_document/)() const | Ottiene o imposta l'oggetto [Document](./get_document/) a cui è collegato questo oggetto. |
| [get_Font](./get_font/)() | Restituisce un oggetto che rappresenta le proprietà di formattazione del carattere corrente. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | Restituisce **true** se il cursore si trova alla fine del paragrafo corrente. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | Restituisce **true** se il cursore si trova alla fine di un tag di documento strutturato. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | Restituisce **true** se il cursore si trova all'inizio del paragrafo corrente (nessun testo prima del cursore). |
| [get_Italic](./get_italic/)() | Vero se il carattere è formattato in corsivo. |
| [get_ListFormat](./get_listformat/)() | Restituisce un oggetto che rappresenta le proprietà di formattazione dell'elenco corrente. |
| [get_PageSetup](./get_pagesetup/)() | Restituisce un oggetto che rappresenta le proprietà di impostazione della pagina e della sezione correnti. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Restituisce un oggetto che rappresenta le proprietà di formattazione del paragrafo corrente. |
| [get_RowFormat](./get_rowformat/)() | Restituisce un oggetto che rappresenta le proprietà di formattazione della riga della tabella corrente. |
| [get_Underline](./get_underline/)() | Ottiene/Imposta il tipo di sottolineatura per il carattere corrente. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | Inserisce un'interruzione del tipo specificato nel documento. |
| [InsertCell](./insertcell/)() | Inserisce una cella di tabella nel documento. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | Inserisce un campo modulo casella di controllo nella posizione corrente. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | Inserisce un campo modulo casella di controllo nella posizione corrente. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | Inserisce un campo modulo casella combinata nella posizione corrente. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Inserisce un documento nella posizione del cursore. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Inserisce un documento nella posizione del cursore. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Inserisce un documento in linea nella posizione del cursore. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | Inserisce un campo Word in un documento e opzionalmente aggiorna il risultato del campo. |
| [InsertField](./insertfield/)(const System::String\&) | Inserisce un campo Word in un documento e aggiorna il risultato del campo. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | Inserisce un campo Word in un documento senza aggiornare il risultato del campo. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | Inserisce una nota a piè di pagina o una nota finale nel documento. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | Inserisce una nota a piè di pagina o una nota finale nel documento. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | Inserisce l'oggetto [Forms2OleControl](../) nella posizione corrente. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Raggruppa le forme passate come parametro in un nuovo nodo GroupShape che viene inserito nella posizione corrente. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Raggruppa le forme passate come parametro in un nuovo nodo GroupShape delle dimensioni specificate che viene inserito nella posizione specificata. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | Inserisce una forma di regola orizzontale nel documento. |
| [InsertHtml](./inserthtml/)(const System::String\&) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | Inserisce una stringa HTML nel documento. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | Inserisce una stringa HTML nel documento. Consente di specificare opzioni aggiuntive. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | Inserisce un collegamento ipertestuale nel documento. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Inserisce un'immagine da un oggetto **Image** nel documento. L'immagine viene inserita in linea e al 100% della scala. |
| [InsertImage](./insertimage/)(const System::String\&) | Inserisce un'immagine da un file o URL nel documento. L'immagine viene inserita in linea e al 100% della scala. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Inserisce un'immagine da un flusso nel documento. L'immagine viene inserita in linea e al 100% della scala. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | Inserisce un'immagine da un array di byte nel documento. L'immagine viene inserita in linea e al 100% della scala. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | Inserisce un'immagine in linea da un oggetto **Image** nel documento e la scala alla dimensione specificata. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | Inserisce un'immagine in linea da un file o URL nel documento e la scala alla dimensione specificata. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | Inserisce un'immagine in linea da un flusso nel documento e la scala alla dimensione specificata. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | Inserisce un'immagine in linea da un array di byte nel documento e la scala alla dimensione specificata. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce un'immagine da un oggetto **Image** nella posizione e dimensione specificate. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce un'immagine da un file o URL nella posizione e dimensione specificate. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce un'immagine da un flusso nella posizione e dimensione specificate. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce un'immagine da un array di byte nella posizione e dimensione specificate. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserisce un nodo prima del cursore. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Inserisce un oggetto OLE incorporato da un flusso nel documento. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE usando l'estensione del file. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE usando il parametro progID fornito. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE usando l'estensione del file. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE usando il parametro progID fornito. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | Inserisce un oggetto OLE incorporato come icona da un flusso nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE usando il parametro progID fornito. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata. |
| [InsertParagraph](./insertparagraph/)() | Inserisce un'interruzione di paragrafo nel documento. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | Inserisce una forma in linea con tipo e dimensione specificati. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserisce una forma fluttuante con posizione, dimensione e tipo di avvolgimento del testo specificati. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | Inserisce una riga di firma nella posizione corrente. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | Inserisce una riga di firma nella posizione specificata. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | Inserisce un [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) nel documento. |
| [InsertStyleSeparator](./insertstyleseparator/)() | Inserisce il separatore di stile nel documento. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | Inserisce un campo TOC (indice) nel documento. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | Inserisce un campo modulo di testo nella posizione corrente. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Sposta il cursore su un nodo inline o alla fine di un paragrafo. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | Sposta il cursore su un segnalibro. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | Sposta il cursore su un segnalibro con maggiore precisione. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | Sposta il cursore su una cella di tabella nella sezione corrente. |
| [MoveToDocumentEnd](./movetodocumentend/)() | Sposta il cursore alla fine del documento. |
| [MoveToDocumentStart](./movetodocumentstart/)() | Sposta il cursore all'inizio del documento. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | Sposta il cursore su un campo nel documento. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | Sposta il cursore all'inizio di un'intestazione o di un piè di pagina nella sezione corrente. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | Sposta il campo di unione sul campo di unione specificato. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | Sposta il cursore su un paragrafo nella sezione corrente. |
| [MoveToSection](./movetosection/)(int32_t) | Sposta il cursore all'inizio del corpo in una sezione specificata. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | Sposta il cursore su un tag di documento strutturato nella sezione corrente. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | Sposta il cursore sul tag di documento strutturato. |
| [PopFont](./popfont/)() | Recupera la formattazione dei caratteri precedentemente salvata nello stack. |
| [PushFont](./pushfont/)() | Salva la formattazione dei caratteri corrente nello stack. |
| [set_Bold](./set_bold/)(bool) | Impostatore per [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Impostatore per [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | Impostatore per [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Impostatore per [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/). |
| [StartBookmark](./startbookmark/)(const System::String\&) | Segna la posizione corrente nel documento come inizio di segnalibro. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | Segna la posizione corrente nel documento come inizio di segnalibro di colonna. La posizione deve trovarsi in una cella di tabella. |
| [StartEditableRange](./starteditablerange/)() | Segna la posizione corrente nel documento come inizio di intervallo modificabile. |
| [StartTable](./starttable/)() | Avvia una tabella nel documento. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | Inserisce una stringa nel documento nella posizione di inserimento corrente. |
| [Writeln](./writeln/)(const System::String\&) | Inserisce una stringa e un'interruzione di paragrafo nel documento. |
| [Writeln](./writeln/)() | Inserisce un'interruzione di paragrafo nel documento. |
## Note


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

Crea un [DocumentBuilder](./) e associarlo a un [Document](../document/).

Il [DocumentBuilder](./) ha un cursore interno dove il testo verrà inserito quando chiami [Write()](../), [Writeln()](../), [InsertBreak()](./insertbreak/) e altri metodi. Puoi spostare il cursore del [DocumentBuilder](./) a una posizione diversa in un documento usando vari metodi MoveToXXX.

Usa la proprietà [Font](./get_font/) per specificare la formattazione dei caratteri che verrà applicata a tutto il testo inserito dalla posizione corrente nel documento in poi.

Usa la proprietà [ParagraphFormat](./get_paragraphformat/) per specificare la formattazione dei paragrafi per quello corrente e per tutti i paragrafi che verranno inseriti.

Usa la proprietà [PageSetup](./get_pagesetup/) per specificare le proprietà di pagina e sezione per la sezione corrente e per tutte le sezioni che verranno inserite.

Usa le proprietà [CellFormat](./get_cellformat/) e [RowFormat](./get_rowformat/) per specificare le proprietà di formattazione per le celle e le righe della tabella. Usa i metodi [InsertCell](./insertcell/) e [EndRow](./endrow/) per costruire una tabella.

Nota che le proprietà [Font](./get_font/), [ParagraphFormat](./get_paragraphformat/) e [PageSetup](./get_pagesetup/) vengono aggiornate ogni volta che ti sposti in un punto diverso del documento per riflettere le proprietà di formattazione disponibili nella nuova posizione.

## Esempi



Mostra come costruire una tabella con bordi personalizzati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Impostazione delle opzioni di formattazione della tabella per un DocumentBuilder
// le applicherà a ogni riga e cella che aggiungiamo con esso.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Modificando la formattazione la applicherà alla cella corrente,
// e a tutte le nuove celle che creiamo con il builder in seguito.
// Questo non influenzerà le celle che abbiamo aggiunto in precedenza.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Aumenta l'altezza della riga per adattare il testo verticale.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Mostra come utilizzare un document builder per creare una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Avvia la tabella, poi popola la prima riga con due celle.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Chiama il metodo "EndRow" del builder per avviare una nuova riga.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
