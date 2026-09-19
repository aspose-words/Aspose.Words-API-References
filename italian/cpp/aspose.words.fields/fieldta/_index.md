---
title: "Aspose::Words::Fields::FieldTA classe"
linktitle: "FieldTA"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldTA classe. Implementa il campo TA. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 99000
url: /it/cpp/aspose.words.fields/fieldta/
---
## FieldTA class


Implementa il campo TA. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldTA : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_EntryCategory](./get_entrycategory/)() | Ottiene la categoria di voce integrale, che è un numero che corrisponde all'ordine delle categorie. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsBold](./get_isbold/)() | Ottiene se applicare la formattazione grassetto al numero di pagina per la voce. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsItalic](./get_isitalic/)() | Ottiene se applicare la formattazione corsivo al numero di pagina per la voce. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_LongCitation](./get_longcitation/)() | Restituisce la citazione lunga per la voce. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | Restituisce il nome del segnalibro che segna un intervallo di pagine inserito come numero di pagina della voce. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_ShortCitation](./get_shortcitation/)() | Restituisce la citazione breve per la voce. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Imposta la categoria integrale della voce, che è un numero che corrisponde all'ordine delle categorie. |
| [set_IsBold](./set_isbold/)(bool) | Imposta se applicare la formattazione grassetto al numero di pagina per la voce. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsItalic](./set_isitalic/)(bool) | Imposta se applicare la formattazione corsivo al numero di pagina per la voce. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LongCitation](./set_longcitation/)(const System::String\&) | Imposta la citazione lunga per la voce. |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String\&) | Imposta il nome del segnalibro che segna un intervallo di pagine inserito come numero di pagina della voce. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ShortCitation](./set_shortcitation/)(const System::String\&) | Imposta la citazione breve per la voce. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
