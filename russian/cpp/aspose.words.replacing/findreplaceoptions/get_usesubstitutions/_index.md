---
title: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions"
linktitle: "get_UseSubstitutions"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions. Получает или задает логическое значение, указывающее, следует ли распознавать и использовать подстановки в шаблонах замены. Значение по умолчанию — false в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


Получает или задает логическое значение, указывающее, следует ли распознавать и использовать подстановки в шаблонах замены. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
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


Показывает, как заменять текст с помощью подстановок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите свойство "UseSubstitutions" в "true", чтобы получить
// операцию поиска и замены, распознающую элементы подстановки.
// Установите свойство "UseSubstitutions" в "false", чтобы игнорировать элементы подстановки.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
