---
title: "Aspose::Words::Markup::SdtListItemCollection класс"
linktitle: "SdtListItemCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::SdtListItemCollection класс. Предоставляет доступ к элементам SdtListItem структурированного тега документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class


Предоставляет доступ к элементам [SdtListItem](../sdtlistitem/) структурированного тега документа. Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SdtListItemCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Добавляет элемент в эту коллекцию. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Очищает все элементы из этой коллекции. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов в коллекции. |
| [get_SelectedValue](./get_selectedvalue/)() | Указывает текущо выбранное значение в этом списке. Допускается значение null, что означает, что ни одна текущо выбранная запись не связана с этой коллекцией элементов списка. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех элементов в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает объект [SdtListItem](../sdtlistitem/), заданный его нулевым индексом в коллекции. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Удаляет элемент списка по указанному индексу. |
| [set_SelectedValue](./set_selectedvalue/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Сеттер для [Aspose::Words::Markup::SdtListItemCollection::get_SelectedValue](./get_selectedvalue/). |
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

## Примеры



Показывает, как работать со structured document tags типа выпадающего списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Элемент structured document tag типа выпадающего списка представляет собой форму, позволяющую пользователю
// выбрать вариант из списка щелчком левой кнопкой мыши и открыть форму в Microsoft Word.
// Свойство "ListItems" содержит все элементы списка, и каждый элемент списка является "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Добавьте ещё 3 элемента списка. Инициализируйте эти элементы, используя другой конструктор, чем у первого элемента
// чтобы отображать строки, отличные от их значений.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// Выпадающий список отображает первый элемент. Присвойте другому элементу списка значение "SelectedValue", чтобы отобразить его.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Переберите коллекцию и выведите каждый элемент.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Удалите последний элемент списка.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Поскольку наш выпадающий элемент управления по умолчанию отображает удалённый элемент, предоставьте ему существующий элемент для отображения.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// Используйте метод "Clear", чтобы очистить всю коллекцию элементов выпадающего списка сразу.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## См. также

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
