---
title: "Classe Aspose::Words::Layout::LayoutOptions"
linktitle: "LayoutOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Layout::LayoutOptions. Contiene le opzioni che consentono di controllare il processo di layout del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Contiene le opzioni che consentono di controllare il processo di layout del documento. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Callback](./get_callback/)() const | Ottiene l'implementazione di [IPageLayoutCallback](../ipagelayoutcallback/) utilizzata dal modello di layout della pagina. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Ottiene o imposta il modo in cui i commenti vengono visualizzati. Il valore predefinito è [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | Ottiene o imposta l'indicazione se l'opzione di compatibilità "Use printer metrics to lay out document" è ignorata. Il valore predefinito è **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | Ottiene o imposta un'indicazione se le metriche originali del carattere devono essere utilizzate dopo la sostituzione del carattere. Il valore predefinito è **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Ottiene le opzioni di revisione. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Ottiene o imposta l'indicazione se il testo nascosto nel documento viene visualizzato. Il valore predefinito è **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Ottiene o imposta l'indicazione se i segni di paragrafo vengono visualizzati. Il valore predefinito è **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Ottiene l'implementazione di [ITextShaperFactory](../) utilizzata per le funzionalità di rendering della tipografia avanzata. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Imposta l'implementazione di [IPageLayoutCallback](../ipagelayoutcallback/) utilizzata dal modello di layout della pagina. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Impostatore per [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Impostatore per [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Impostatore per [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | Impostatore per [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Impostatore per [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Impostatore per [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Imposta l'implementazione di [ITextShaperFactory](../) utilizzata per le funzionalità di rendering della tipografia avanzata. |
| static [Type](./type/)() |  |
## Note


Non è possibile creare istanze di questa classe direttamente. Usa la proprietà [LayoutOptions](../../aspose.words/document/get_layoutoptions/) per accedere alle opzioni di layout per questo documento.

Nota che dopo aver modificato una qualsiasi delle opzioni presenti in questa classe, il metodo [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) dovrebbe essere chiamato affinché le opzioni modificate vengano applicate al layout.

## Esempi



Mostra come nascondere il testo in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci testo nascosto, quindi specifica se desideriamo ometterlo da un documento renderizzato.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Mostra come visualizzare i segni di paragrafo in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare le fine dei paragrafi
// con il simbolo pilcrow (¶) quando renderizziamo il documento.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Rimuovi la barra che appare a sinistra di ogni riga revisionata.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
