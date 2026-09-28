---
title: "Aspose::Words::Fields::DropDownItemCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::DropDownItemCollection::RemoveAt method. Удаляет значение по указанному индексу в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.fields/dropdownitemcollection/removeat/
---
## DropDownItemCollection::RemoveAt method


Удаляет значение по указанному индексу.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::RemoveAt(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Нулевой индекс. |

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

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
