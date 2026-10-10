---
title: "Aspose::Words::Fields::FieldRef::get_BookmarkName metodo"
linktitle: "get_BookmarkName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldRef::get_BookmarkName metodo. Restituisce o imposta il nome del segnalibro di riferimento in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldref/get_bookmarkname/
---
## FieldRef::get_BookmarkName method


Ottiene o imposta il nome del segnalibro di riferimento.

```cpp
System::String Aspose::Words::Fields::FieldRef::get_BookmarkName()
```


## Esempi



Mostra come creare testo contrassegnato con un campo SET e poi visualizzarlo nel documento usando un campo REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nomina il testo contrassegnato con un campo SET.
// Questo campo si riferisce al "bookmark" non a una struttura di segnalibro che appare nel testo, ma a una variabile nominata.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Fai riferimento al segnalibro per nome in un campo REF e visualizza il suo contenuto.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Vedi anche

* Class [FieldRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
