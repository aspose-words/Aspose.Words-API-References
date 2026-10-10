---
title: "Aspose::Words::Fields::FieldDdeAuto classe"
linktitle: "FieldDdeAuto"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldDdeAuto classe. Implementa il campo DDEAUTO. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words.fields/fieldddeauto/
---
## FieldDdeAuto class


Implementa il campo DDEAUTO. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDdeAuto : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Ottiene se inserire l'oggetto collegato come bitmap. |
| [get_InsertAsHtml](./get_insertashtml/)() | Ottiene se inserire l'oggetto collegato come testo in formato HTML. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Ottiene se inserire l'oggetto collegato come immagine. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Ottiene se inserire l'oggetto collegato in formato rich-text (RTF). |
| [get_InsertAsText](./get_insertastext/)() | Ottiene se inserire l'oggetto collegato in formato solo testo. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Ottiene se inserire l'oggetto collegato come testo Unicode. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLinked](./get_islinked/)() | Ottiene se ridurre le dimensioni del file non memorizzando i dati grafici con il documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_ProgId](./get_progid/)() | Ottiene il tipo di applicazione delle informazioni del collegamento. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | Ottiene il nome e la posizione del file sorgente. |
| [get_SourceItem](./get_sourceitem/)() | Ottiene la porzione del file sorgente che è collegata. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Imposta se inserire l'oggetto collegato come bitmap. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Imposta se inserire l'oggetto collegato come testo in formato HTML. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Imposta se inserire l'oggetto collegato come immagine. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Imposta se inserire l'oggetto collegato in formato rich-text (RTF). |
| [set_InsertAsText](./set_insertastext/)(bool) | Imposta se inserire l'oggetto collegato in formato solo testo. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Imposta se inserire l'oggetto collegato come testo Unicode. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Imposta se ridurre le dimensioni del file non memorizzando i dati grafici nel documento. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Imposta il tipo di applicazione delle informazioni di collegamento. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Imposta il nome e la posizione del file di origine. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Imposta la porzione del file di origine che viene collegata. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
