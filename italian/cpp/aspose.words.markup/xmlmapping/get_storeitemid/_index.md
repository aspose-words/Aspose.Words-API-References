---
title: "Aspose::Words::Markup::XmlMapping::get_StoreItemId metodo"
linktitle: "get_StoreItemId"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::XmlMapping::get_StoreItemId metodo. Specifica l'identificatore dei dati XML personalizzati per la parte di dati XML personalizzata che sarà usato per valutare l'espressione XPath in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Specificare l'identificatore dei dati XML personalizzati per la parte di dati XML personalizzata che sarà usato per valutare l'espressione [XPath](../get_xpath/).

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Esempi



Mostra come ottenere l'identificatore dei dati XML personalizzati di una parte XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// Le etichette di documento strutturato hanno ID sotto forma di GUID.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## Vedi anche

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
