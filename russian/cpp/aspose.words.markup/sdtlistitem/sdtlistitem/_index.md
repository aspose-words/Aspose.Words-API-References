---
title: "Aspose::Words::Markup::SdtListItem::SdtListItem конструктор"
linktitle: "SdtListItem"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::SdtListItem::SdtListItem конструктор. Инициализирует новый экземпляр этого класса в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.markup/sdtlistitem/sdtlistitem/
---
## SdtListItem::SdtListItem(const System::String\&, const System::String\&) constructor


Инициализирует новый экземпляр этого класса.

```cpp
Aspose::Words::Markup::SdtListItem::SdtListItem(const System::String &displayText, const System::String &value)
```


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

* Class [SdtListItem](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
## SdtListItem::SdtListItem(const System::String\&) constructor


Инициализирует новый экземпляр этого класса.

```cpp
Aspose::Words::Markup::SdtListItem::SdtListItem(const System::String &value)
```


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

* Class [SdtListItem](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
