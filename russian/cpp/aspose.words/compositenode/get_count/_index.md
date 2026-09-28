---
title: "Метод Aspose::Words::CompositeNode::get_Count"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::CompositeNode::get_Count. Получает количество непосредственных дочерних узлов этого узла в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/compositenode/get_count/
---
## CompositeNode::get_Count method


Возвращает количество непосредственных дочерних элементов этого узла.

```cpp
int32_t Aspose::Words::CompositeNode::get_Count()
```


## Примеры



Показывает, как добавить, обновить и удалить дочерние узлы в коллекции детей [CompositeNode](../)'s.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ по умолчанию содержит один абзац.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Создайте ещё три узла run.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Тело документа не будет отображать эти run'ы, пока мы не вставим их в составной узел
// который сам является частью дерева узлов документа, как мы сделали с первым run.
// Мы можем определить, где будет находиться текстовое содержимое узлов, которые мы вставляем
// в документе, указав место вставки относительно другого узла в абзаце.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Вставьте второй run в абзац перед начальным run.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Вставьте третий run после начального run.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Вставьте первый run в начало коллекции дочерних узлов абзаца.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Мы можем изменить содержимое run, редактируя и удаляя существующие дочерние узлы.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## См. также

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
