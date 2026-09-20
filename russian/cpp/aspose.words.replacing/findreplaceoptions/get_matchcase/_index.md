---
title: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase"
linktitle: "get_MatchCase"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase. True указывает на чувствительное к регистру сравнение, false указывает на нечувствительное к регистру сравнение в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True указывает на сравнение с учётом регистра, false указывает на сравнение без учёта регистра.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Примеры



Показывает, как переключать чувствительность к регистру при выполнении операции поиска и замены.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "MatchCase" в значение "true", чтобы применять чувствительность к регистру при поиске строк для замены.
// Установите флаг "MatchCase" в значение "false", чтобы игнорировать регистр символов при поиске текста для замены.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
