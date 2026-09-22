---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged yöntemi"
linktitle: "get_HyperlinksChanged"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged yöntemi. Bir belgedeki hiperlinklerin C++'ta değiştirildiğini gösterir."
type: docs
weight: 13500
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


Bir belgedeki bağlantıların değişip değişmediğini gösterir.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
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
