---
title: "Класс Aspose::Words::MailMerging::MappedDataFieldCollection"
linktitle: "MappedDataFieldCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::MailMerging::MappedDataFieldCollection. Позволяет автоматически сопоставлять имена полей в вашем источнике данных с именами полей слияния в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Позволяет автоматически сопоставлять имена полей в вашем источнике данных с именами полей слияния почты в документе. Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Добавляет новое сопоставление полей. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Удаляет все элементы из коллекции. |
| [ContainsKey](./containskey/)(const System::String\&) | Определяет, существует ли сопоставление указанного поля в документе в коллекции. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Определяет, существует ли сопоставление указанного поля в источнике данных в коллекции. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество элементов, содержащихся в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя словаря, который можно использовать для перебора всех элементов коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Получает или задает имя поля в источнике данных, связанное с указанным полем слияния. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Получает или задает имя поля в источнике данных, связанное с указанным полем слияния. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Удаляет сопоставление полей. |
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


Это реализовано как коллекция строковых ключей и строковых значений. Ключи — это имена полей слияния в документе, а значения — имена полей в вашем источнике данных.

## См. также

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
