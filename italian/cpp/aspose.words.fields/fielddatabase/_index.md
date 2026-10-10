---
title: "Aspose::Words::Fields::FieldDatabase classe"
linktitle: "FieldDatabase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldDatabase classe. Implementa il campo DATABASE. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


Implementa il campo DATABASE. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | Ottiene una connessione ai dati. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_FileName](./get_filename/)() | Ottiene il percorso completo e il nome file del database. |
| [get_FirstRecord](./get_firstrecord/)() | Ottiene il numero intero del record del primo dato da inserire. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_FormatAttributes](./get_formatattributes/)() | Ottiene quali attributi del formato devono essere applicati alla tabella. |
| [get_InsertHeadings](./get_insertheadings/)() | Ottiene se inserire i nomi dei campi dal database come intestazioni di colonna nella tabella risultante. |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | Ottiene se inserire i dati all'inizio di una fusione. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LastRecord](./get_lastrecord/)() | Ottiene il numero intero del record dell'ultimo dato da inserire. |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Query](./get_query/)() | Ottiene un insieme di istruzioni SQL che interrogano il database. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_TableFormat](./get_tableformat/)() | Ottiene il formato da applicare al risultato della query del database. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_Connection](./set_connection/)(const System::String\&) | Imposta una connessione ai dati. |
| [set_FileName](./set_filename/)(const System::String\&) | Imposta il percorso completo e il nome file del database. |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | Imposta il numero intero del record del primo dato da inserire. |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | Imposta quali attributi del formato devono essere applicati alla tabella. |
| [set_InsertHeadings](./set_insertheadings/)(bool) | Imposta se inserire i nomi dei campi dal database come intestazioni di colonna nella tabella risultante. |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | Imposta se inserire i dati all'inizio di una fusione. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | Imposta il numero intero del record dell'ultimo dato da inserire. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Query](./set_query/)(const System::String\&) | Imposta un insieme di istruzioni SQL che interrogano il database. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | Imposta il formato da applicare al risultato della query del database. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
