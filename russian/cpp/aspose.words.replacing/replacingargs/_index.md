---
title: "Класс Aspose::Words::Replacing::ReplacingArgs"
linktitle: "ReplacingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Replacing::ReplacingArgs. Предоставляет данные для пользовательской операции замены. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


Предоставляет данные для пользовательской операции замены. Чтобы узнать больше, посетите статью документации [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class ReplacingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | Определяет, по индексу, захваченную группу в [Match](./get_match/), которую нужно заменить строкой [Replacement](./get_replacement/). |
| [get_GroupName](./get_groupname/)() const | Определяет, по имени, захваченную группу в [Match](./get_match/), которую нужно заменить строкой [Replacement](./get_replacement/). |
| [get_Match](./get_match/)() const | Объект **Match**, полученный в результате единственного сопоставления регулярного выражения во время **Replace**. |
| [get_MatchEndNode](./get_matchendnode/)() const | Получает узел, содержащий конец совпадения. |
| [get_MatchNode](./get_matchnode/)() const | Получает узел, содержащий начало совпадения. |
| [get_MatchOffset](./get_matchoffset/)() const | Получает нулевой индекс начальной позиции совпадения от начала узла, содержащего начало совпадения. |
| [get_Replacement](./get_replacement/)() const | Получает строку замены. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | Сеттер для [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/). |
| [set_GroupName](./set_groupname/)(const System::String\&) | Сеттер для [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/). |
| [set_Replacement](./set_replacement/)(const System::String\&) | Устанавливает строку замены. |
| static [Type](./type/)() |  |

## См. также

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
