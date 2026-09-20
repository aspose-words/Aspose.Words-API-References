---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection::Contains метод"
linktitle: "Contains"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection::Contains метод. Определяет, содержит ли коллекция свойство с заданным именем в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.markup/customxmlpropertycollection/contains/
---
## CustomXmlPropertyCollection::Contains method


Определяет, содержит ли коллекция свойство с заданным именем.

```cpp
bool Aspose::Words::Markup::CustomXmlPropertyCollection::Contains(const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Чувствительное к регистру имя свойства для поиска. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

## Примеры



Показывает, как работать со свойствами смарт‑тегов, чтобы получить подробную информацию о смарт‑тегах.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// Смарт‑тег появляется в документе, когда Microsoft Word распознаёт часть его текста как определённый тип данных,
// например, имя, дату или адрес, и преобразует его в гиперссылку, отображающуюся пурпурным пунктирным подчёркиванием.
// В Word 2003 можно включить смарт‑теги через "Tools" -> "AutoCorrect options..." -> "SmartTags".
// В нашем входном документе есть три объекта, которые Microsoft Word зарегистрировал как смарт‑теги.
// Смарт‑теги могут быть вложенными, поэтому эта коллекция содержит больше элементов.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// Член "Properties" смарт‑тега содержит его метаданные, которые будут различаться для каждого типа смарт‑тега.
// Свойства смарт‑тега типа "date" содержат его год, месяц и день.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// Мы также можем получать доступ к свойствам различными способами, например, как пара ключ‑значение.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Ниже представлены три способа удаления элементов из коллекции свойств.
// 1 -  Удалить по индексу:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  Удалить по имени:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Очистить всю коллекцию сразу:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## См. также

* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
