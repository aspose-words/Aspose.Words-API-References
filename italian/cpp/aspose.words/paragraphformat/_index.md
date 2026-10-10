---
title: "Classe Aspose::Words::ParagraphFormat"
linktitle: "ParagraphFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::ParagraphFormat. Rappresenta tutta la formattazione di un paragrafo. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 49000
url: /it/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Rappresenta tutta la formattazione di un paragrafo. Per saperne di più, visita l'articolo di documentazione [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Ripristina la formattazione del paragrafo predefinita. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Ottiene o imposta un flag che indica se la spaziatura intercarattere è regolata automaticamente tra regioni di testo latino e regioni di testo dell'Asia orientale nel paragrafo corrente. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Ottiene o imposta un flag che indica se la spaziatura intercarattere è regolata automaticamente tra regioni di numeri e regioni di testo dell'Asia orientale nel paragrafo corrente. |
| [get_Alignment](./get_alignment/)() | Ottiene o imposta l'allineamento del testo per il paragrafo. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Ottiene o imposta la posizione verticale dei font su una riga. |
| [get_Bidi](./get_bidi/)() | Ottiene o imposta se questo è un paragrafo da destra a sinistra. |
| [get_Borders](./get_borders/)() | Ottiene la raccolta dei bordi del paragrafo. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | Ottiene o imposta il valore (in caratteri) per il rientro della prima riga o sospeso. Usa valori positivi per impostare il rientro della prima riga e valori negativi per impostare il rientro sospeso. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Ottiene o imposta il valore del rientro sinistro (in caratteri) per i paragrafi specificati. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Ottiene o imposta il valore del rientro destro (in caratteri) per i paragrafi specificati. |
| [get_DropCapPosition](./get_dropcapposition/)() | Ottiene o imposta la posizione per un testo drop cap. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Ottiene o imposta un flag che indica se le regole di interruzione di riga dell'Asia orientale sono applicate al paragrafo corrente. |
| [get_FirstLineIndent](./get_firstlineindent/)() | Ottiene o imposta il valore (in punti) per un rientro della prima riga o sospeso. Usa valori positivi per impostare il rientro della prima riga e valori negativi per impostare il rientro sospeso. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Ottiene o imposta un flag che indica se la punteggiatura sospesa è abilitata per il paragrafo corrente. |
| [get_IsHeading](./get_isheading/)() | Vero quando lo stile del paragrafo è uno degli stili di intestazione incorporati. |
| [get_IsListItem](./get_islistitem/)() | Vero quando il paragrafo è un elemento in un elenco puntato o numerato. |
| [get_KeepTogether](./get_keeptogether/)() | Vero se tutte le righe del paragrafo devono rimanere nella stessa pagina. |
| [get_KeepWithNext](./get_keepwithnext/)() | Vero se il paragrafo deve rimanere nella stessa pagina del paragrafo che lo segue. |
| [get_LeftIndent](./get_leftindent/)() | Ottiene o imposta il valore (in punti) che rappresenta il rientro sinistro per il paragrafo. |
| [get_LineSpacing](./get_linespacing/)() | Ottiene o imposta l'interlinea (in punti) per il paragrafo. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Ottiene o imposta l'interlinea per il paragrafo. |
| [get_LinesToDrop](./get_linestodrop/)() | Ottiene o imposta il numero di righe del testo del paragrafo usate per calcolare l'altezza del drop cap. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Ottiene o imposta la quantità di spazio (in linee di griglia) dopo i paragrafi. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Ottiene o imposta la quantità di spazio (in linee di griglia) prima dei paragrafi. |
| [get_MirrorIndents](./get_mirrorindents/)() | Ottiene o imposta un flag che indica se i rientri sinistro e destro hanno la stessa larghezza. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | Quando **true**, [SpaceBefore](./get_spacebefore/) e [SpaceAfter](./get_spaceafter/) saranno ignorati tra i paragrafi dello stesso stile. |
| [get_OutlineLevel](./get_outlinelevel/)() | Specifica il livello di struttura del paragrafo nel documento. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | Vero se viene forzata un'interruzione di pagina prima del paragrafo. |
| [get_RightIndent](./get_rightindent/)() | Ottiene o imposta il valore (in punti) che rappresenta il rientro destro per il paragrafo. |
| [get_Shading](./get_shading/)() | Restituisce un oggetto [Shading](../shading/) che si riferisce alla formattazione dell'ombreggiatura per il paragrafo. |
| [get_SnapToGrid](./get_snaptogrid/)() | Specifica se il paragrafo corrente deve utilizzare le impostazioni delle linee della griglia del documento per pagina durante il layout del contenuto nel paragrafo. |
| [get_SpaceAfter](./get_spaceafter/)() | Ottiene o imposta la quantità di spaziatura (in punti) dopo il paragrafo. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | Vero se la quantità di spaziatura dopo il paragrafo è impostata automaticamente. |
| [get_SpaceBefore](./get_spacebefore/)() | Ottiene o imposta la quantità di spaziatura (in punti) prima del paragrafo. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | Vero se la quantità di spaziatura prima del paragrafo è impostata automaticamente. |
| [get_Style](./get_style/)() | Ottiene o imposta lo stile di paragrafo applicato a questa formattazione. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile di paragrafo applicato a questa formattazione. |
| [get_StyleName](./get_stylename/)() | Ottiene o imposta il nome dello stile di paragrafo applicato a questa formattazione. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Specifica se il paragrafo corrente deve essere esentato da qualsiasi sillabazione applicata nelle impostazioni del documento. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Specifica se le righe del paragrafo corrente devono essere esentate dalla numerazione delle righe applicata nella sezione padre. |
| [get_TabStops](./get_tabstops/)() | Ottiene la raccolta di tabulazioni personalizzate definite per questo oggetto. |
| [get_WidowControl](./get_widowcontrol/)() | Vero se la prima e l'ultima riga del paragrafo devono rimanere sulla stessa pagina del resto del paragrafo. |
| [get_WordWrap](./get_wordwrap/)() | Se questa proprietà è **false**, il testo latino al centro di una parola può essere interrotto per il paragrafo corrente. Altrimenti il testo latino è interrotto per parole intere. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Impostatore per [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | Impostatore per [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/). |
| [set_Bidi](./set_bidi/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | Impostatore per [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Impostatore per [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Impostatore per [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Impostatore per [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Impostatore per [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Impostatore per [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Impostatore per [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Impostatore per [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Impostatore per [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come costruire manualmente un documento Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e otterrai un nodo documento senza figli.
doc->RemoveAllChildren();

// Questo documento ora non ha nodi figli compositi a cui possiamo aggiungere contenuti.
// Se desideriamo modificarlo, dovremo ripopolare la sua collezione di nodi.
// Per prima cosa, crea una nuova sezione, quindi aggiungila come figlio al nodo radice del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Imposta alcune proprietà di configurazione della pagina per la sezione.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutti i suoi contenuti
// sulla pagina tra l'intestazione e il piè di pagina della sezione.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi aggiungilo come figlio al corpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Infine, aggiungi del contenuto al documento. Crea un run,
// imposta il suo aspetto e i suoi contenuti, e quindi aggiungilo come figlio al paragrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
