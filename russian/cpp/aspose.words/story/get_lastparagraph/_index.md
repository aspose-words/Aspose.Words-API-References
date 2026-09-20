---
title: "Aspose::Words::Story::get_LastParagraph method"
linktitle: "get_LastParagraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Story::get_LastParagraph method. Возвращает последний абзац в истории в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Возвращает последний абзац в истории.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## Примеры



Показывает, как переместить позицию курсора [DocumentBuilder](../../documentbuilder/) к указанному узлу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// У построителя документа есть курсор, который выступает частью документа
// где построитель добавляет новые узлы, когда мы используем его методы построения документа.
// Этот курсор работает так же, как мигающий курсор Microsoft Word,
// и он также всегда оказывается сразу после любого узла, который построитель только что вставил.
// Чтобы добавить содержимое в другую часть документа,
// мы можем переместить курсор к другому узлу с помощью метода "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// Курсор теперь находится перед узлом, к которому мы его переместили.
// Добавление второго фрагмента вставит его перед первым фрагментом.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Переместите курсор в конец документа, чтобы продолжить добавлять текст в конец, как и раньше.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## См. также

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
