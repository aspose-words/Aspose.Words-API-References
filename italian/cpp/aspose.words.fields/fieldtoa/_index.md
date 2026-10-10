---
title: "Aspose::Words::Fields::FieldToa classe"
linktitle: "FieldToa"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldToa classe. Implementa il campo TOA. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 104000
url: /it/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


Implementa il campo TOA. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Ottiene il nome del segnalibro che contrassegna la parte del documento utilizzata per costruire la tabella. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_EntryCategory](./get_entrycategory/)() | Ottiene la categoria integrale per le voci incluse nella tabella. |
| [get_EntrySeparator](./get_entryseparator/)() | Ottiene la sequenza di caratteri utilizzata per separare una voce della tabella delle autorità dal suo numero di pagina. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Ottiene la sequenza di caratteri utilizzata per separare due numeri di pagina in un elenco di numeri di pagina. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Ottiene la sequenza di caratteri utilizzata per separare l'inizio e la fine di un intervallo di pagine. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Ottiene se rimuovere la formattazione del testo della voce nel documento dalla voce nella tabella delle autorità. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_SequenceName](./get_sequencename/)() | Ottiene il nome di una sequenza il cui numero è incluso con il numero di pagina. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Ottiene la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [get_UseHeading](./get_useheading/)() | Ottiene se includere l'intestazione della categoria per le voci in una tabella delle autorità. |
| [get_UsePassim](./get_usepassim/)() | Ottiene se sostituire cinque o più riferimenti di pagina diversi alla stessa autorità con "passim", che è usato per indicare che una parola o passaggio compare frequentemente nell'opera citata. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per costruire la tabella. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Imposta la categoria integrale per le voci incluse nella tabella. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Imposta la sequenza di caratteri utilizzata per separare una voce della tabella delle autorità dal suo numero di pagina. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Imposta la sequenza di caratteri utilizzata per separare due numeri di pagina in un elenco di numeri di pagina. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Imposta la sequenza di caratteri utilizzata per separare l'inizio e la fine di un intervallo di pagine. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Imposta se rimuovere la formattazione del testo della voce nel documento dalla voce nella tabella delle autorità. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Imposta il nome di una sequenza il cui numero è incluso con il numero di pagina. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [set_UseHeading](./set_useheading/)(bool) | Imposta se includere l'intestazione della categoria per le voci in una tabella delle autorità. |
| [set_UsePassim](./set_usepassim/)(bool) | Imposta se sostituire cinque o più riferimenti di pagina diversi alla stessa autorità con "passim", che viene usato per indicare che una parola o un passaggio compare frequentemente nell'opera citata. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
