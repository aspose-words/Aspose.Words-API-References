---
title: "Метод Aspose::Words::Markup::XmlMapping::get_StoreItemId"
linktitle: "get_StoreItemId"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::XmlMapping::get_StoreItemId. Указывает идентификатор пользовательских XML‑данных для пользовательской части XML, который будет использоваться для оценки выражения XPath в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Указывает идентификатор пользовательских XML‑данных для пользовательской части XML, который будет использоваться для оценки выражения [XPath](../get_xpath/).

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Примеры



Показывает, как получить идентификатор пользовательских XML‑данных части XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// Теги структурированных документов имеют идентификаторы в виде GUID.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## См. также

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
