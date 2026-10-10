---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument yöntemi"
linktitle: "get_SharedDocument"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument yöntemi. Belgenin paylaşılan bir belge olup olmadığını C++'ta gösterir."
type: docs
weight: 25500
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_shareddocument/
---
## BuiltInDocumentProperties::get_SharedDocument method


Belgenin paylaşılan bir belge olup olmadığını gösterir.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument()
```

## Açıklamalar


Aspose.Words bu özelliği güncellemez.

## Örnekler



Genişletilmiş özelliklerin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
