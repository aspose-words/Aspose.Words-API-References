---
title: "Aspose::Words::Fields::FieldMergeField classe"
linktitle: "FieldMergeField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldMergeField classe. Implementa il campo MERGEFIELD. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 67000
url: /it/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


Implementa il campo MERGEFIELD. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldName](./get_fieldname/)() | Ottiene il nome di un campo dati. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | Restituisce solo il nome del campo dati. Qualsiasi prefisso viene rimosso nella proprietà prefix. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_IsMapped](./get_ismapped/)() | Ottiene se questo campo è un campo mappato. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | Ottiene se abilitare la conversione dei caratteri per la formattazione verticale. |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_TextAfter](./get_textafter/)() | Ottiene il testo da inserire dopo il campo se il campo non è vuoto. |
| [get_TextBefore](./get_textbefore/)() | Ottiene il testo da inserire prima del campo se il campo non è vuoto. |
| [get_Type](./get_type/)() const override | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | Imposta il nome di un campo dati. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsMapped](./set_ismapped/)(bool) | Imposta se questo campo è un campo mappato. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | Imposta se abilitare la conversione dei caratteri per la formattazione verticale. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TextAfter](./set_textafter/)(const System::String\&) | Imposta il testo da inserire dopo il campo se il campo non è vuoto. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | Imposta il testo da inserire prima del campo se il campo non è vuoto. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
