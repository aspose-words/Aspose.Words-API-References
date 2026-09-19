---
title: "classe Aspose::Words::Fields::FieldToc"
linktitle: "FieldToc"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Fields::FieldToc. Implementa il campo TOC. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 105000
url: /it/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


Implementa il campo TOC. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Ottiene il nome del segnalibro che contrassegna la parte del documento utilizzata per costruire la tabella. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Ottiene o imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure che non include l'etichetta e il numero della didascalia. |
| [get_CustomStyles](./get_customstyles/)() | Ottiene un elenco di stili diversi dagli stili di intestazione predefiniti da includere nella tabella dei contenuti. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Ottiene una stringa che deve corrispondere agli identificatori di tipo dei campi TC inclusi. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Ottiene un intervallo di livelli delle voci della tabella dei contenuti da includere. |
| [get_EntrySeparator](./get_entryseparator/)() | Ottiene una sequenza di caratteri che separano una voce dal suo numero di pagina. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Ottiene un intervallo di livelli di intestazione da includere. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Ottiene se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Ottiene se rendere le voci della tabella dei contenuti collegamenti ipertestuali. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Ottiene un intervallo di livelli delle voci della tabella dei contenuti da cui omettere i numeri di pagina. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Ottiene o imposta l'identificatore di una sequenza per la quale dovrebbe essere aggiunto un prefisso al numero di pagina della voce. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Ottiene se preservare i caratteri di nuova riga all'interno delle voci della tabella. |
| [get_PreserveTabs](./get_preservetabs/)() | Ottiene se preservare le tabulazioni all'interno delle voci della tabella. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Ottiene o imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Ottiene se utilizzare il livello di contorno del paragrafo applicato. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per costruire la tabella. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Setter per [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Imposta un elenco di stili diversi dagli stili di intestazione predefiniti da includere nella tabella dei contenuti. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Imposta una stringa che deve corrispondere agli identificatori di tipo dei campi TC inclusi. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Imposta un intervallo di livelli delle voci della tabella dei contenuti da includere. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Imposta una sequenza di caratteri che separano una voce dal suo numero di pagina. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Imposta un intervallo di livelli di intestazione da includere. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Imposta se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Imposta se rendere le voci della tabella dei contenuti collegamenti ipertestuali. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Imposta un intervallo di livelli delle voci del sommario da cui omettere i numeri di pagina. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Imposta se conservare i caratteri di nuova riga all'interno delle voci della tabella. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Imposta se conservare le tabulazioni all'interno delle voci della tabella. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Imposta se utilizzare il livello di contorno del paragrafo applicato. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Aggiorna i numeri di pagina per gli elementi di questo indice. |

## Esempi



Mostra come popolare un campo TOC con voci usando i campi SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che include il campo SEQ e il numero di pagina in cui il campo appare.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// I campi SEQ mostrano un conteggio che incrementa ad ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza nominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Usa la proprietà "TableOfFiguresLabel" per denominare una sequenza principale per il TOC.
// Ora, questo TOC creerà solo voci da campi SEQ il cui "SequenceIdentifier" è impostato su "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Possiamo denominare un'altra sequenza di campo SEQ nella proprietà "PrefixedSequenceIdentifier".
// I campi SEQ di questa sequenza prefisso non creeranno voci nel TOC.
// Ogni voce del TOC creata da un campo SEQ di sequenza principale ora visualizzerà anche il conteggio che
// la sequenza prefisso è attualmente al valore del campo SEQ di sequenza primaria che ha generato la voce.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Ogni voce del TOC visualizzerà il conteggio della sequenza prefisso immediatamente a sinistra
// del numero di pagina su cui appare il campo SEQ della sequenza principale.
// Possiamo specificare un separatore personalizzato che apparirà tra questi due numeri.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Esistono due modi per utilizzare i campi SEQ per popolare questo TOC.
// 1 -  Inserimento di un campo SEQ che appartiene alla sequenza prefisso del TOC:
// Questo campo incrementerà il conteggio della sequenza SEQ per "PrefixSequence" di 1.
// Poiché questo campo non appartiene alla sequenza principale identificata
// dalla proprietà "TableOfFiguresLabel" del TOC, non apparirà come voce.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Inserimento di un campo SEQ che appartiene alla sequenza principale del TOC:
// Questo campo SEQ creerà una voce nel TOC.
// La voce del TOC conterrà il paragrafo in cui si trova il campo SEQ e il numero della pagina su cui appare.
// Questa voce visualizzerà anche il conteggio attuale della sequenza prefisso,
// separato dal numero di pagina dal valore nella proprietà SeqenceSeparator del TOC.
// Il conteggio "PrefixSequence" è a 1, questo campo SEQ della sequenza principale è a pagina 2,
// e il separatore è ">", quindi la voce visualizzerà "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Inserisci una pagina, avanza la sequenza prefisso di 2 e inserisci un campo SEQ per creare una voce del TOC successivamente.
// La sequenza prefisso è ora a 2, e il campo SEQ della sequenza principale è a pagina 3,
// quindi la voce del TOC visualizzerà "2>3" nel suo conteggio di pagina.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
