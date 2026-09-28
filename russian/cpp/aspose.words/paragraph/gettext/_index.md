---
title: "Метод Aspose::Words::Paragraph::GetText"
linktitle: "GetText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::GetText method. Получает текст этого абзаца, включая символ конца абзаца, в C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words/paragraph/gettext/
---
## Paragraph::GetText method


Получает текст этого абзаца, включая символ конца абзаца.

```cpp
System::String Aspose::Words::Paragraph::GetText() override
```

## Примечания


Текст всех дочерних узлов конкатенируется, и символ конца абзаца добавляется следующим образом:

* If the paragraph is the last paragraph of [Body](../../body/), then [SectionBreak](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then [Cell](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [ParagraphBreak](../../controlchar/paragraphbreak/) (\r) is appended.



Возвращаемая строка включает все управляющие и специальные символы, как описано в [ControlChar](../../controlchar/).

## Примеры



Показывает, как добавить, обновить и удалить дочерние узлы в коллекции дочерних элементов [CompositeNode](../../compositenode/).
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
