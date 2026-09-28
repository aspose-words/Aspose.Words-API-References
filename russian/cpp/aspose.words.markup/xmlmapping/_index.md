---
title: "Aspose::Words::Markup::XmlMapping class"
linktitle: "XmlMapping"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::XmlMapping class. Указывает информацию, используемую для установления сопоставления между родительским структурированным тегом документа и элементом XML, хранящимся в пользовательской части XML‑данных в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


Указывает информацию, используемую для установления сопоставления между родительским структурным тегом документа и элементом XML, хранящимся в пользовательской части данных XML в документе. Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class XmlMapping : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Delete](./delete/)() | Удаляет сопоставление родительского структурированного документа с XML‑данными. |
| [get_CustomXmlPart](./get_customxmlpart/)() | Возвращает пользовательскую часть XML‑данных, к которой сопоставлен родительский структурированный тег документа. |
| [get_IsMapped](./get_ismapped/)() | Возвращает **true**, если родительский структурированный тег документа успешно сопоставлен с XML‑данными. |
| [get_PrefixMappings](./get_prefixmappings/)() const | Возвращает сопоставления префиксов пространств имён XML для оценки [XPath](./get_xpath/). |
| [get_StoreItemId](./get_storeitemid/)() | Указывает идентификатор пользовательских XML‑данных для пользовательской части XML, которая будет использоваться для оценки выражения [XPath](./get_xpath/). |
| [get_XPath](./get_xpath/)() const | Возвращает выражение XPath, которое оценивается для поиска пользовательского узла XML, сопоставленного с родительским структурированным тегом документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | Устанавливает сопоставление между родительским структурированным тегом документа и узлом XML пользовательской части XML‑данных. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
