---
title: "Aspose::Words::Fields::FieldAuthor classe"
linktitle: "FieldAuthor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldAuthor classe. Implementa il campo AUTHOR. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.fields/fieldauthor/
---
## FieldAuthor class


Implementa il campo AUTHOR. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAuthor : public Aspose::Words::Fields::Field
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AuthorName](./get_authorname/)() | Ottiene o imposta il nome dell'autore del documento. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_AuthorName](./set_authorname/)(const System::String\&) | Setter per [Aspose::Words::Fields::FieldAuthor::get_AuthorName](./get_authorname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come utilizzare un campo AUTHOR per visualizzare il nome del creatore del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// I campi AUTHOR ottengono i loro risultati dalla proprietà di documento incorporata chiamata "Author".
// Se creiamo e salviamo un documento in Microsoft Word,
// avrà il nostro nome utente in quella proprietà.
// Tuttavia, se creiamo un documento programmaticamente usando Aspose.Words,
// la proprietà "Author", per impostazione predefinita, sarà una stringa vuota.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Imposta un nome autore di backup da utilizzare per i campi AUTHOR
// se la proprietà "Author" contiene una stringa vuota.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Aggiornare un campo AUTHOR che contiene un valore
// applicherà quel valore alla proprietà incorporata "Author".
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Modificando questa proprietà, quindi aggiornando il campo AUTHOR, si applicherà questo valore al campo.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// Se aggiorniamo un campo AUTHOR dopo aver cambiato la sua proprietà "Name",
// quindi il campo visualizzerà il nuovo nome e applicherà il nuovo nome alla proprietà incorporata.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// I campi AUTHOR non influiscono sulla proprietà DefaultDocumentAuthor.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
