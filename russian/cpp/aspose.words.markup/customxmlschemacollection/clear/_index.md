---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::Clear метод"
linktitle: "Clear"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::Clear метод. Удаляет все элементы из коллекции в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.markup/customxmlschemacollection/clear/
---
## CustomXmlSchemaCollection::Clear method


Удаляет все элементы из коллекции.

```cpp
void Aspose::Words::Markup::CustomXmlSchemaCollection::Clear()
```


## Примеры



Показывает, как работать с коллекцией XML‑схем.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Добавьте ассоциацию XML‑схемы.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Клонируйте коллекцию ассоциаций XML‑схем пользовательской части XML,
// а затем добавьте несколько новых схем в клон.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Переберите схемы и выведите каждый элемент.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Ниже представлены три способа удаления схем из коллекции.
// 1 -  Удалить схему по индексу:
schemas->RemoveAt(2);

// 2 -  Удалить схему по значению:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Используйте метод "Clear", чтобы очистить коллекцию сразу.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## См. также

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
