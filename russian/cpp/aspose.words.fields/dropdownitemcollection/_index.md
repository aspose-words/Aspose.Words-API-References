---
title: "Aspose::Words::Fields::DropDownItemCollection класс"
linktitle: "DropDownItemCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::DropDownItemCollection класс. Коллекция строк, представляющих все элементы в раскрывающемся поле формы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


Коллекция строк, представляющих все элементы выпадающего поля формы. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::String\&) | Добавляет строку в конец коллекции. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Удаляет все элементы из коллекции. |
| [Contains](./contains/)(const System::String\&) | Определяет, содержит ли коллекция указанное значение. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех элементов в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает или задает элемент по указанному индексу. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Получает или задает элемент по указанному индексу. |
| [IndexOf](./indexof/)(const System::String\&) | Возвращает нулевой индекс указанного значения в коллекции. |
| [Insert](./insert/)(int32_t, const System::String\&) | Вставляет строку в коллекцию по указанному индексу. |
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

## Примеры



Показывает, как вставить поле комбинированного списка и отредактировать элементы в его коллекции.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте комбинированный список, а затем проверьте его коллекцию раскрывающихся элементов.
// В Microsoft Word пользователь щелкнет по комбинированному списку,
// а затем выберет один из текстовых элементов в коллекции для отображения.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Существует два способа добавить новый элемент в существующую коллекцию элементов раскрывающегося списка.
// 1 -  Добавить элемент в конец коллекции:
dropDownItems->Add(u"Four");

// 2 -  Вставить элемент перед другим элементом по указанному индексу:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Итерировать коллекцию и вывести каждый элемент.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Существует два способа удаления элементов из коллекции раскрывающихся элементов.
// 1 -  Удалить элемент, содержимое которого равно переданной строке:
dropDownItems->Remove(u"Four");

// 2 -  Удалить элемент по индексу:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Очистить всю коллекцию раскрывающихся элементов.
dropDownItems->Clear();
```

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
