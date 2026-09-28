---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes метод"
linktitle: "get_IgnoreFootnotes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes. Получает или задает логическое значение, указывающее, следует ли игнорировать сноски. Значение по умолчанию — false в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


Получает или задает логическое значение, указывающее, следует ли игнорировать сноски. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Примеры



Показывает, как игнорировать сноски во время операции поиска и замены.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Установите флаг "IgnoreFootnotes" в "true", чтобы выполнить поиск и замену
// операцию, игнорирующую текст внутри сносок.
// Установите флаг "IgnoreFootnotes" в "false", чтобы выполнить поиск и замену
// операцию, также ищущую текст внутри сносок.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
