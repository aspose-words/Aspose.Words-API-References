---
title: "Класс Aspose::Words::Markup::CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Markup::CustomXmlSchemaCollection. Коллекция строк, представляющих XML‑схемы, связанные с пользовательской частью XML. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


Коллекция строк, представляющих XML‑схемы, связанные с пользовательской XML‑частью. Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::String\&) | Добавляет элемент в коллекцию. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Удаляет все элементы из коллекции. |
| [Clone](./clone/)() | Создаёт глубокую копию этого объекта. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех элементов в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает или задает элемент по указанному индексу. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Получает или задает элемент по указанному индексу. |
| [IndexOf](./indexof/)(const System::String\&) | Возвращает нулевой индекс указанного значения в коллекции. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Удаляет указанное значение из коллекции. |
| [RemoveAt](./removeat/)(int32_t) | Удаляет значение по указанному индексу. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Типовое определение | Описание |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Примечания


Вы не создаёте экземпляры этого класса. Вы получаете доступ к коллекции XML‑схем пользовательской части XML через свойство [Schemas](../customxmlpart/get_schemas/).

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
