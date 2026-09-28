---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping метод"
linktitle: "get_XmlMapping"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping метод. Возвращает объект, представляющий сопоставление этого диапазона структурированного тега документа с XML-данными в пользовательской части XML текущего документа в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Получает объект, представляющий сопоставление диапазона этого структурированного тега документа с XML‑данными в пользовательской части XML текущего документа.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Примеры



Показывает, как установить XML-соответствия для начала диапазона структурированного тега документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// Создайте часть XML, содержащую текст, и добавьте её в коллекцию CustomXmlPart документа.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Создайте структурированный тег документа, который будет отображать содержимое нашего CustomXmlPart в документе.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// Если мы зададим сопоставление для нашего структурированного тега документа,
// он будет отображать только часть CustomXmlPart, на которую указывает XPath.
// Этот XPath будет указывать на содержимое второго элемента "<text>" первого элемента "<root>" нашего CustomXmlPart.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## См. также

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
