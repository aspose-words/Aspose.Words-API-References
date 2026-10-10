---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument metodo"
linktitle: "get_SharedDocument"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument metodo. Indica se il documento è un documento condiviso in C++."
type: docs
weight: 25500
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_shareddocument/
---
## BuiltInDocumentProperties::get_SharedDocument method


Indica se il documento è un documento condiviso.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument()
```

## Note


Aspose.Words non aggiorna questa proprietà.

## Esempi



Mostra come ottenere le proprietà estese.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
