---
title: "Aspose::Words::Fields::FieldSectionPages classe"
linktitle: "FieldSectionPages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldSectionPages classe. Implementa il campo SECTIONPAGES. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 89000
url: /it/cpp/aspose.words.fields/fieldsectionpages/
---
## FieldSectionPages class


Implementa il campo SECTIONPAGES. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldSectionPages : public Aspose::Words::Fields::Field
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
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
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come utilizzare i campi SECTION e SECTIONPAGES per numerare le pagine per sezioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Un campo SECTION visualizza il numero della sezione in cui si trova.
builder->Write(u"Section ");
auto fieldSection = System::ExplicitCast<Aspose::Words::Fields::FieldSection>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSection, true));

ASSERT_EQ(u" SECTION ", fieldSection->GetFieldCode());

// Un campo PAGE visualizza il numero della pagina in cui si trova.
builder->Write(u"\nPage ");
auto fieldPage = System::ExplicitCast<Aspose::Words::Fields::FieldPage>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, true));

ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// Un campo SECTIONPAGES visualizza il numero di pagine che la sezione in cui si trova copre.
builder->Write(u" of ");
auto fieldSectionPages = System::ExplicitCast<Aspose::Words::Fields::FieldSectionPages>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSectionPages, true));

ASSERT_EQ(u" SECTIONPAGES ", fieldSectionPages->GetFieldCode());

// Esci dall'intestazione, torna al documento principale e inserisci due pagine.
// Tutte queste pagine saranno nella prima sezione. I nostri campi, che appaiono una volta per ogni intestazione,
// numereranno le pagine attuali/totali di questa sezione.
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Possiamo inserire una nuova sezione con il costruttore di documenti in questo modo.
// Questo influenzerà i valori visualizzati nei campi SECTION e SECTIONPAGES in tutte le intestazioni successive.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

// Il campo PAGE continuerà a contare le pagine in tutto il documento.
// Possiamo reimpostare manualmente il suo conteggio in ogni sezione per tenere traccia delle pagine sezione per sezione.
builder->get_CurrentSection()->get_PageSetup()->set_RestartPageNumbering(true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SECTION.SECTIONPAGES.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
