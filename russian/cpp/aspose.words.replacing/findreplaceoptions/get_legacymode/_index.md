---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode метод"
linktitle: "get_LegacyMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode метод. Получает или задает логическое значение, указывающее, что используется старый алгоритм поиска/замены в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Получает или задает логическое значение, указывающее, что используется старый алгоритм поиска/замены.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
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
