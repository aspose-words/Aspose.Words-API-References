---
title: "Aspose::Words::Fields::FieldAuthor::get_AuthorName metodo"
linktitle: "get_AuthorName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldAuthor::get_AuthorName metodo. Ottiene o imposta il nome dell'autore del documento in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldauthor/get_authorname/
---
## FieldAuthor::get_AuthorName method


Ottiene o imposta il nome dell'autore del documento.

```cpp
System::String Aspose::Words::Fields::FieldAuthor::get_AuthorName()
```


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

* Class [FieldAuthor](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
