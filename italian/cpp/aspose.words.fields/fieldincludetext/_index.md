---
title: "Aspose::Words::Fields::FieldIncludeText classe"
linktitle: "FieldIncludeText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldIncludeText classe. Implementa il campo INCLUDETEXT. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Implementa il campo INCLUDETEXT. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Ottiene il nome del segnalibro nel documento da includere. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_Encoding](./get_encoding/)() | Ottiene la codifica applicata ai dati nel file di riferimento. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_LockFields](./get_lockfields/)() override | Ottiene se impedire l'aggiornamento dei campi nel documento incluso. |
| [get_MimeType](./get_mimetype/)() | Ottiene il tipo MIME del file di riferimento. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Ottiene le mappature degli spazi dei nomi per le query XPath. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Ottiene l'ubicazione del documento usando un IRI. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_TextConverter](./get_textconverter/)() override | Ottiene il nome del convertitore di testo per il formato del file incluso. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [get_XPath](./get_xpath/)() override | Ottiene XPath per la parte desiderata del file XML. |
| [get_XslTransformation](./get_xsltransformation/)() override | Ottiene l'ubicazione della trasformazione XSL per formattare i dati XML. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Imposta il nome del segnalibro nel documento da includere. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Imposta la codifica applicata ai dati nel file di riferimento. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Imposta se impedire l'aggiornamento dei campi nel documento incluso. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Imposta il tipo MIME del file di riferimento. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Imposta le mappature degli spazi dei nomi per le query XPath. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Imposta l'ubicazione del documento usando un IRI. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Imposta il nome del convertitore di testo per il formato del file incluso. |
| [set_XPath](./set_xpath/)(const System::String\&) | Imposta l'XPath per la parte desiderata del file XML. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Imposta la posizione della trasformazione XSL per formattare i dati XML. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
