---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection класс"
linktitle: "BaseWebExtensionCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection класс. Базовый класс для коллекций TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection и WebExtensionReferenceCollection. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


Базовый класс для коллекций [TaskPaneCollection](../taskpanecollection/), [WebExtensionBindingCollection](../webextensionbindingcollection/), [WebExtensionPropertyCollection](../webextensionpropertycollection/) и [WebExtensionReferenceCollection](../webextensionreferencecollection/). Чтобы узнать больше, посетите статью документации [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| Параметр | Описание |
| --- | --- |
| T | Тип элемента коллекции. |
## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(T) | Добавляет указанный элемент в коллекцию. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Удаляет все элементы из коллекции. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает перечислитель, который может проходить по коллекции. |
| [idx_get](./idx_get/)(int32_t) | Получает или задает элемент по указанному индексу. |
| [idx_set](./idx_set/)(int32_t, T) | Получает или задает элемент по указанному индексу. |
| [Remove](./remove/)(int32_t) | Удаляет элемент по указанному индексу из коллекции. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
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



Показывает, как работать с коллекцией веб‑расширений документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Выводит все свойства веб‑расширения документа.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Удалить веб-расширение.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## См. также

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
