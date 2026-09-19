---
title: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes metodo"
linktitle: "get_IsInMegabytes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes metodo. Ottiene o imposta se visualizzare la dimensione del file in megabyte in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldfilesize/get_isinmegabytes/
---
## FieldFileSize::get_IsInMegabytes method


Ottiene o imposta se visualizzare la dimensione del file in megabyte.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes()
```


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

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
