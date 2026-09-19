---
title: "Aspose::Words::Fields::FieldCitation classe"
linktitle: "FieldCitation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldCitation classe. Implementa il campo CITATION. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Implementa il campo CITATION. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Ottiene un valore che corrisponde al valore dell'elemento **Tag** di un'altra fonte da includere nella citazione. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Ottiene l'ID lingua utilizzato in combinazione con lo stile bibliografico specificato per formattare la citazione nel documento. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_PageNumber](./get_pagenumber/)() | Ottiene un numero di pagina associato alla citazione. |
| [get_Prefix](./get_prefix/)() | Ottiene un prefisso che viene anteposto alla citazione. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_SourceTag](./get_sourcetag/)() | Ottiene un valore che corrisponde al valore dell'elemento **Tag** della fonte da inserire. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Suffix](./get_suffix/)() | Ottiene un suffisso che viene aggiunto alla citazione. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Ottiene se le informazioni sull'autore sono nascoste nella citazione. |
| [get_SuppressTitle](./get_suppresstitle/)() | Ottiene se le informazioni sul titolo sono nascoste nella citazione. |
| [get_SuppressYear](./get_suppressyear/)() | Ottiene se le informazioni sull'anno sono nascoste nella citazione. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [get_VolumeNumber](./get_volumenumber/)() | Ottiene un numero di volume associato alla citazione. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Imposta un valore che corrisponde al valore dell'elemento **Tag** di un'altra fonte da includere nella citazione. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Imposta l'ID lingua utilizzato in combinazione con lo stile bibliografico specificato per formattare la citazione nel documento. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Imposta un numero di pagina associato alla citazione. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Imposta un prefisso che viene anteposto alla citazione. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Imposta un valore che corrisponde al valore dell'elemento **Tag** della fonte da inserire. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Imposta un suffisso che viene aggiunto alla citazione. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Imposta se le informazioni sull'autore sono nascoste nella citazione. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Imposta se le informazioni sul titolo sono nascoste nella citazione. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Imposta se le informazioni sull'anno sono nascoste nella citazione. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Imposta un numero di volume associato alla citazione. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
