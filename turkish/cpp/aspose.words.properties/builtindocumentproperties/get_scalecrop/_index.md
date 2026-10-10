---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop metodu"
linktitle: "get_ScaleCrop"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop metodu. Belge küçük resminin görüntüye sığması için kırpılmış mı yoksa ölçeklendirilmiş mi olduğunu C++'da gösterir."
type: docs
weight: 24500
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


Belge küçük resminin kırpılıp kırpılmadığını veya ekrana sığacak şekilde ölçeklendirilip ölçeklendirilmediğini gösterir.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
