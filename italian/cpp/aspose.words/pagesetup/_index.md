---
title: "classe Aspose::Words::PageSetup"
linktitle: "PageSetup"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::PageSetup. Rappresenta le proprietà di configurazione della pagina di una sezione. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 46000
url: /it/cpp/aspose.words/pagesetup/
---
## PageSetup class


Rappresenta le proprietà di configurazione della pagina di una sezione. Per saperne di più, visita l'articolo di documentazione [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Ripristina la configurazione della pagina alle dimensioni della carta, ai margini e all'orientamento predefiniti. |
| [get_Bidi](./get_bidi/)() | Specifica che questa sezione contiene testo bidirezionale (script complessi). |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Specifica dove il bordo della pagina è posizionato rispetto a testi e oggetti intersecanti. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Specifica su quali pagine il bordo della pagina viene stampato. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Ottiene o imposta un valore che indica se il bordo della pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda. |
| [get_Borders](./get_borders/)() | Ottiene una raccolta dei bordi della pagina. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Specifica se il bordo della pagina include o esclude il piè di pagina. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Specifica se il bordo della pagina include o esclude l'intestazione. |
| [get_BottomMargin](./get_bottommargin/)() | Restituisce o imposta la distanza (in punti) tra il bordo inferiore della pagina e il limite inferiore del testo del corpo. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Ottiene o imposta il carattere separatore che appare tra il numero del capitolo e il numero di pagina. |
| [get_CharactersPerLine](./get_charactersperline/)() | Ottiene o imposta il numero di caratteri per riga nella griglia del documento. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | Vero se un'intestazione o un piè di pagina diverso è usato nella prima pagina. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Fornisce opzioni che controllano la numerazione e il posizionamento delle note finali in questa sezione. |
| [get_FirstPageTray](./get_firstpagetray/)() | Ottiene il vassoio di carta (contenitore) da utilizzare per la prima pagina di una sezione. Il valore è specifico dell'implementazione (stampante). |
| [get_FooterDistance](./get_footerdistance/)() | Restituisce o imposta la distanza (in punti) tra il piè di pagina e il bordo inferiore della pagina. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questa sezione. |
| [get_Gutter](./get_gutter/)() | Ottiene o imposta la quantità di spazio extra aggiunto al margine per la rilegatura del documento. |
| [get_HeaderDistance](./get_headerdistance/)() | Restituisce o imposta la distanza (in punti) tra l'intestazione e la parte superiore della pagina. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Ottiene o imposta lo stile di livello di intestazione applicato ai titoli dei capitoli nel documento. |
| [get_LayoutMode](./get_layoutmode/)() | Ottiene o imposta la modalità di layout di questa sezione. |
| [get_LeftMargin](./get_leftmargin/)() | Restituisce o imposta la distanza (in punti) tra il bordo sinistro della pagina e il confine sinistro del testo principale. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Restituisce o imposta l'incremento numerico per i numeri di riga. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Ottiene o imposta la distanza tra il bordo destro dei numeri di riga e il bordo sinistro del documento. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Ottiene o imposta il modo in cui la numerazione delle righe avviene, cioè se ricomincia all'inizio di una nuova pagina o sezione o se continua ininterrottamente. |
| [get_LinesPerPage](./get_linesperpage/)() | Ottiene o imposta il numero di righe per pagina nella griglia del documento. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Ottiene o imposta il numero di riga iniziale. |
| [get_Margins](./get_margins/)() | Restituisce o imposta i [Margini](../margins/) predefiniti della pagina. |
| [get_MultiplePages](./get_multiplepages/)() const | Per i documenti a più pagine, ottiene o imposta come un documento viene stampato o renderizzato in modo da poter essere rilegato come opuscolo. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | Vero se il documento ha intestazioni e piè di pagina diversi per le pagine dispari e pari. |
| [get_Orientation](./get_orientation/)() | Restituisce o imposta l'orientamento della pagina. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Ottiene il vassoio di carta (contenitore) da utilizzare per tutte le pagine tranne la prima di una sezione. Il valore è specifico dell'implementazione (stampante). |
| [get_PageHeight](./get_pageheight/)() | Restituisce o imposta l'altezza della pagina in punti. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Ottiene o imposta il formato del numero di pagina. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Ottiene o imposta il numero di pagina iniziale della sezione. |
| [get_PageWidth](./get_pagewidth/)() | Restituisce o imposta la larghezza della pagina in punti. |
| [get_PaperSize](./get_papersize/)() | Restituisce o imposta le dimensioni della carta. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | Vero se la numerazione delle pagine ricomincia all'inizio della sezione. |
| [get_RightMargin](./get_rightmargin/)() | Restituisce o imposta la distanza (in punti) tra il bordo destro della pagina e il confine destro del testo del corpo. |
| [get_RtlGutter](./get_rtlgutter/)() | Ottiene o imposta se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra. |
| [get_SectionStart](./get_sectionstart/)() | Restituisce o imposta il tipo di interruzione di sezione per l'oggetto specificato. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Restituisce o imposta il numero di pagine da includere in ogni opuscolo. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | Vero se le note finali vengono stampate alla fine della sezione successiva che non sopprime le note finali. Le note finali sopresse vengono stampate prima delle note finali in quella sezione. |
| [get_TextColumns](./get_textcolumns/)() | Restituisce una raccolta che rappresenta l'insieme delle colonne di testo. |
| [get_TextOrientation](./get_textorientation/)() | Consente di specificare [TextOrientation](./get_textorientation/) per l'intera pagina. Il valore predefinito è [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | Restituisce o imposta la distanza (in punti) tra il bordo superiore della pagina e il confine superiore del testo del corpo. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Restituisce o imposta l'allineamento verticale del testo su ogni pagina in un documento o sezione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | Impostatore per [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | Impostatore per [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | Impostatore per [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | Impostatore per [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | Impostatore per [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Imposta il vassoio della carta (contenitore) da utilizzare per la prima pagina di una sezione. Il valore è specifico dell'implementazione (stampante). |
| [set_FooterDistance](./set_footerdistance/)(double) | Impostatore per [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | Impostatore per [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | Impostatore per [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Impostatore per [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Impostatore per [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Impostatore per [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Impostatore per [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Impostatore per [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Impostatore per [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Impostatore per [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Impostatore per [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | Impostatore per [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Impostatore per [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Impostatore per [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Imposta il vassoio della carta (bin) da utilizzare per tutte le pagine tranne la prima di una sezione. Il valore è specifico dell'implementazione (stampante). |
| [set_PageHeight](./set_pageheight/)(double) | Impostatore per [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Impostatore per [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Impostatore per [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Impostatore per [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Impostatore per [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Impostatore per [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Impostatore per [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Impostatore per [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Impostatore per [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | Vero se le note finali vengono stampate alla fine della sezione successiva che non sopprime le note finali. Le note finali sopresse vengono stampate prima delle note finali in quella sezione. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Impostatore per [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Impostatore per [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Impostatore per [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## Note


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Esempi



Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifica le proprietà di configurazione della pagina per la sezione corrente del builder e aggiungi testo.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Se avviamo una nuova sezione utilizzando un document builder,
// eredità le proprietà di configurazione della pagina correnti del builder.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Possiamo ripristinare le sue proprietà di configurazione della pagina ai valori predefiniti usando il metodo "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
