---
title: "Aspose::Words::Markup::CustomXmlPartCollection::idx_set метод"
linktitle: "idx_set"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::CustomXmlPartCollection::idx_set метод. Получает или задаёт элемент по указанному индексу в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.markup/customxmlpartcollection/idx_set/
---
## CustomXmlPartCollection::idx_set method


Получает или задает элемент по указанному индексу.

```cpp
void Aspose::Words::Markup::CustomXmlPartCollection::idx_set(int32_t index, const System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> &value)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Нулевой индекс элемента. |

## Примеры



Показывает, как создать структурированный тег документа с пользовательскими XML-данными.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте XML‑часть, содержащую данные, и добавьте её в коллекцию документа.
// Если включить вкладку "Developer" в Microsoft Word,
// мы можем найти элементы этой коллекции в "XML Mapping Pane", вместе с несколькими элементами по умолчанию.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Ниже представлены два способа обращения к XML‑частям.
// 1 -  По индексу в коллекции пользовательских XML‑частей:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  По GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Добавьте ассоциацию XML‑схемы.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Клонируйте часть, а затем вставьте её в коллекцию.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Итерируйте по коллекции и выводите содержимое каждой части.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Используйте метод "RemoveAt" для удаления клонированной части по индексу.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Клонируйте коллекцию XML‑частей, а затем используйте метод "Clear" для одновременного удаления всех её элементов.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Создайте структурированный тег документа, который будет отображать содержимое нашей части, и вставьте его в тело документа.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## См. также

* Class [CustomXmlPart](../../customxmlpart/)
* Class [CustomXmlPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
