---
title: "Класс Aspose::Words::VariableCollection"
linktitle: "VariableCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::VariableCollection. Коллекция переменных документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 73000
url: /ru/cpp/aspose.words/variablecollection/
---
## VariableCollection class


Коллекция переменных документа. Чтобы узнать больше, посетите статью документации [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class VariableCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Добавляет переменную документа в коллекцию. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Удаляет все элементы из коллекции. |
| [Contains](./contains/)(const System::String\&) | Определяет, содержит ли коллекция переменную документа с указанным именем. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех переменных в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Получает или задает переменную документа по нечувствительному к регистру имени. Значения **null** не допускаются в правой части присваивания и будут заменены пустой строкой. |
| [idx_get](./idx_get/)(int32_t) | Получает или задает переменную документа по указанному индексу. Значения **null** не допускаются в правой части присваивания и будут заменены пустой строкой. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Получает или задает переменную документа по нечувствительному к регистру имени. Значения **null** не допускаются в правой части присваивания и будут заменены пустой строкой. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Получает или задает переменную документа по указанному индексу. Значения **null** не допускаются в правой части присваивания и будут заменены пустой строкой. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Возвращает нулевой индекс указанной переменной документа в коллекции. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Удаляет переменную документа с указанным именем из коллекции. |
| [RemoveAt](./removeat/)(int32_t) | Удаляет переменную документа по указанному индексу. |
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


Имена и значения переменных являются строками.

Имена переменных нечувствительны к регистру.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
