---
title: "Метод Aspose::Words::Lists::ListLevel::GetEffectiveValue"
linktitle: "GetEffectiveValue"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Lists::ListLevel::GetEffectiveValue. Возвращает строковое представление объекта ListLevel для указанного индекса элемента списка. Параметры указывают NumberStyle и необязательную строку формата, используемую при указании Custom в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


Возвращает строковое представление объекта [ListLevel](../) для указанного индекса элемента списка. Параметры задают [NumberStyle](../../../aspose.words/numberstyle/) и необязательную строку формата, используемую, когда указано [Custom](../../../aspose.words/numberstyle/).

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс элемента списка (должен находиться в диапазоне от 1 до 32767). |
| numberStyle | Aspose::Words::NumberStyle | [NumberStyle](../../../aspose.words/numberstyle/) объекта [ListLevel](../). |
| customNumberStyleFormat | const System::String\& | Необязательная строка формата, используемая, когда указано [Custom](../../../aspose.words/numberstyle/) (например, \"a, ç, ĝ, ...\"). В остальных случаях этот параметр должен быть **null** или пустым. |

### ReturnValue

Строковое представление объекта [ListLevel](../), описанное параметрами *numberStyle* и *customNumberStyleFormat*, в элементе списка на позиции, определяемой параметром *index*.

## Примеры



Показывает, как получить формат списка с пользовательским стилем нумерации.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// Мы можем получить значение для указанного индекса элемента списка.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```

## См. также

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
