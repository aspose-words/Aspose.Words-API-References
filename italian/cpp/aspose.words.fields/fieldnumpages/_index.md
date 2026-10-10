---
title: "Classe Aspose::Words::Fields::FieldNumPages"
linktitle: "FieldNumPages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fields::FieldNumPages. Implementa il campo NUMPAGES. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 74000
url: /it/cpp/aspose.words.fields/fieldnumpages/
---
## FieldNumPages class


Implementa il campo NUMPAGES. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldNumPages : public Aspose::Words::Fields::Field
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



Mostra come utilizzare i campi NUMCHARS, NUMWORDS, NUMPAGES e PAGE per tenere traccia delle dimensioni dei nostri documenti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Di seguito sono riportati tre tipi di campi che possiamo utilizzare per tenere traccia delle dimensioni dei nostri documenti.
// 1 -  Traccia il conteggio dei caratteri con un campo NUMCHARS:
auto fieldNumChars = System::ExplicitCast<Aspose::Words::Fields::FieldNumChars>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumChars, true));
builder->Writeln(u" characters");

// 2 -  Traccia il conteggio delle parole con un campo NUMWORDS:
auto fieldNumWords = System::ExplicitCast<Aspose::Words::Fields::FieldNumWords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumWords, true));
builder->Writeln(u" words");

// 3 -  Usa entrambi i campi PAGE e NUMPAGES per visualizzare su quale pagina si trova il campo,
// e il numero totale di pagine nel documento:
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Page ");
auto fieldPage = System::ExplicitCast<Aspose::Words::Fields::FieldPage>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, true));
builder->Write(u" of ");
auto fieldNumPages = System::ExplicitCast<Aspose::Words::Fields::FieldNumPages>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumPages, true));

ASSERT_EQ(u" NUMCHARS ", fieldNumChars->GetFieldCode());
ASSERT_EQ(u" NUMWORDS ", fieldNumWords->GetFieldCode());
ASSERT_EQ(u" NUMPAGES ", fieldNumPages->GetFieldCode());
ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// Questi campi non manterranno valori accurati in tempo reale
// mentre modifichiamo il documento programmaticamente usando Aspose.Words, o in Microsoft Word.
// Dobbiamo aggiornarli ogni volta che abbiamo bisogno di vedere un valore aggiornato.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
