---
title: "Метод Aspose::Words::Markup::XmlMapping::Delete"
linktitle: "Удалить"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::XmlMapping::Delete. Удаляет сопоставление родительского структурированного документа с XML‑данными в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.markup/xmlmapping/delete/
---
## XmlMapping::Delete method


Удаляет сопоставление родительского структурированного документа с XML‑данными.

```cpp
void Aspose::Words::Markup::XmlMapping::Delete()
```


## Примеры



Показывает, как задать сопоставления XML для пользовательских частей XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте часть XML, содержащую текст, и добавьте её в коллекцию CustomXmlPart документа.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Создайте структурированный тег документа, который будет отображать содержимое нашего CustomXmlPart.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// Установите сопоставление для нашего структурированного тега документа. Это сопоставление будет указывать
// нашему структурированному тегу документа отображать часть текстового содержимого части XML, на которую указывает XPath.
// В этом случае это будет содержимое второго элемента "<text>" первого элемента "<root>": "Text element #2".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Добавьте структурированный тег документа в документ, чтобы отобразить содержимое из нашей пользовательской части.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## См. также

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
