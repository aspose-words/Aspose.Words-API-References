---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly метод"
linktitle: "get_FindWholeWordsOnly"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly метод. True указывает, что oldValue должно быть отдельным словом в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True указывает, что oldValue должен быть отдельным словом.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Примеры



Показывает, как переключать операции поиска и замены только отдельными словами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "FindWholeWordsOnly" в значение "true", чтобы заменять найденный текст, если он не является частью другого слова.
// Установите флаг "FindWholeWordsOnly" в значение "false", чтобы заменять весь текст независимо от его окружения.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
