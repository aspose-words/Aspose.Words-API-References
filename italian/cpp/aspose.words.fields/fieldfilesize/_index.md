---
title: "Classe Aspose::Words::Fields::FieldFileSize"
linktitle: "FieldFileSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fields::FieldFileSize. Implementa il campo FILESIZE. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words.fields/fieldfilesize/
---
## FieldFileSize class


Implementa il campo FILESIZE. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldFileSize : public Aspose::Words::Fields::Field,
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
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsInKilobytes](./get_isinkilobytes/)() | Ottiene o imposta se visualizzare la dimensione del file in kilobyte. |
| [get_IsInMegabytes](./get_isinmegabytes/)() | Ottiene o imposta se visualizzare la dimensione del file in megabyte. |
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
| [set_IsInKilobytes](./set_isinkilobytes/)(bool) | Impostatore per [Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes](./get_isinkilobytes/). |
| [set_IsInMegabytes](./set_isinmegabytes/)(bool) | Impostatore per [Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes](./get_isinmegabytes/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Note


Recupera la dimensione del file del documento corrente o 0 se la dimensione non può essere determinata.

Nell'implementazione corrente, utilizza la proprietà [OriginalFileName](../../aspose.words/document/get_originalfilename/) per recuperare il nome del file usato per determinare la dimensione del file.

## Esempi



Mostra come visualizzare la dimensione del file di un documento con un campo FILESIZE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Di seguito sono riportate tre diverse unità di misura
// con le quali i campi FILESIZE possono visualizzare la dimensione del file del documento.
// 1 -  Byte:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobyte:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabyte:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// Per aggiornare i valori di questi campi durante la modifica in Microsoft Word,
// dobbiamo prima salvare le modifiche, quindi aggiornare manualmente questi campi.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
