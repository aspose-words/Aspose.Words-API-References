---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged metodo"
linktitle: "get_HyperlinksChanged"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged metodo. Indica se i collegamenti ipertestuali in un documento sono stati modificati in C++."
type: docs
weight: 13500
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


Indica se i collegamenti ipertestuali in un documento sono stati modificati.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
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
