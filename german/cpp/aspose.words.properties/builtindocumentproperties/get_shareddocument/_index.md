---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument Methode"
linktitle: "get_SharedDocument"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument Methode. Gibt an, ob das Dokument ein gemeinsam genutztes Dokument in C++ ist."
type: docs
weight: 25500
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_shareddocument/
---
## BuiltInDocumentProperties::get_SharedDocument method


Gibt an, ob das Dokument ein freigegebenes Dokument ist.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument()
```

## Hinweise


Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele



Zeigt, wie erweiterte Eigenschaften abgerufen werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
