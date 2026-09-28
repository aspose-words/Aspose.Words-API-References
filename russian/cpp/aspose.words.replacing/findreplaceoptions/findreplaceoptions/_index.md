---
title: "Конструктор Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions. Инициализирует новый экземпляр класса FindReplaceOptions с настройками по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


Инициализирует новый экземпляр класса [FindReplaceOptions](../) с настройками по умолчанию.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
```


## Примеры



Показывает, как распознавать и использовать подстановки в шаблонах замены.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Использование устаревшего режима не поддерживает многие расширенные возможности, поэтому нам нужно установить его в 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


Инициализирует новый экземпляр класса [FindReplaceOptions](../) с указанным направлением.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| направление | Aspose::Words::Replacing::FindReplaceDirection | Направление операции поиска и замены. |

## См. также

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Инициализирует новый экземпляр класса [FindReplaceOptions](../) с указанным направлением и обратным вызовом замены.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| направление | Aspose::Words::Replacing::FindReplaceDirection | Направление операции поиска и замены. |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | Обратный вызов, используемый для замены найденного текста. |

## См. также

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Инициализирует новый экземпляр класса [FindReplaceOptions](../) с указанным обратным вызовом замены.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | Обратный вызов, используемый для замены найденного текста. |

## См. также

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
