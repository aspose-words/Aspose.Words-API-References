---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted метод"
linktitle: "get_IgnoreInserted"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted метод. Получает или задает логическое значение, указывающее, игнорировать ли текст внутри вставок ревизий. Значение по умолчанию — false в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри вставленных правок. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## Примеры



Показывает, как включать или игнорировать текст внутри вставок ревизий во время операции поиска и замены.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Начните отслеживание ревизий и вставьте абзац. Этот абзац будет вставкой ревизии.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "IgnoreInserted" в значение "true", чтобы выполнить поиск и замену
// операцию, игнорирующую абзацы, являющиеся вставками ревизий.
// Установите флаг "IgnoreInserted" в значение "false", чтобы выполнить поиск и замену
// операцию, также ищущую текст внутри вставок ревизий.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
