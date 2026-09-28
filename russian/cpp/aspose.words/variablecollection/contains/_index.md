---
title: "Метод Aspose::Words::VariableCollection::Contains"
linktitle: "Contains"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::VariableCollection::Contains. Определяет, содержит ли коллекция переменную документа с заданным именем в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/variablecollection/contains/
---
## VariableCollection::Contains method


Определяет, содержит ли коллекция переменную документа с указанным именем.

```cpp
bool Aspose::Words::VariableCollection::Contains(const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Нечувствительное к регистру имя переменной документа для поиска. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.

## Примеры



Показывает, как работать с коллекцией переменных документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// У каждого документа есть коллекция переменных в виде пар «ключ/значение», в которую мы можем добавлять элементы.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Мы можем отображать значения переменных в теле документа, используя поля DOCVARIABLE.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Присвоение значений существующим ключам обновит их.
variables->Add(u"Home address", u"456 Queen St.");

// Затем нам потребуется обновить поля DOCVARIABLE, чтобы они отображали актуальное значение.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Проверьте, что переменные документа с определённым именем или значением существуют.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// Коллекция переменных автоматически сортирует их в алфавитном порядке по имени.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Переберите коллекцию переменных.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Ниже представлены три способа удаления переменных документа из коллекции.
// 1 -  По имени:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  По индексу:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Очистить всю коллекцию сразу:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## См. также

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
