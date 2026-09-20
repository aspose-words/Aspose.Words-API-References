---
title: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted"
linktitle: "get_IgnoreDeleted"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted. Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри удалённых правок. Значение по умолчанию — false в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри удалённых правок. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Примеры



Показывает, как включать или игнорировать текст внутри удалённых правок во время операции поиска и замены.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Начните отслеживание правок и удалите второй абзац, что создаст правку удаления.
// Этот абзац останется в документе, пока мы не примем правку удаления.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "IgnoreDeleted" в "true", чтобы выполнить поиск и замену
// операцию, игнорирующую абзацы, являющиеся правками удаления.
// Установите флаг "IgnoreDeleted" в "false", чтобы выполнить поиск и замену
// операцию, также ищущую текст внутри правок удаления.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## См. также

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
