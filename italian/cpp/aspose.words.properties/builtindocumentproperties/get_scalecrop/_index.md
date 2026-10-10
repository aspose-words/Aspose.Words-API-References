---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop metodo"
linktitle: "get_ScaleCrop"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop metodo. Indica se la miniatura del documento è ritagliata o scalata per adattarsi alla visualizzazione in C++."
type: docs
weight: 24500
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


Indica se la miniatura del documento è ritagliata o scalata per adattarsi allo schermo.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
