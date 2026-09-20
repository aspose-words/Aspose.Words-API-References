---
title: "Aspose::Words::DocumentBuilder::MoveTo method"
linktitle: "MoveTo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::MoveTo method. Перемещает курсор к встроенному узлу или в конец абзаца в C++."
type: docs
weight: 51000
url: /ru/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


Перемещает курсор к встроенному узлу или в конец абзаца.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| узел | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел должен быть абзацем или прямым дочерним элементом абзаца. |
## Примечания


Когда *node* является встроенным узлом, курсор перемещается к этому узлу, и последующее содержимое будет вставлено перед этим узлом.

Когда *node* является [Paragraph](../../paragraph/), курсор перемещается в конец абзаца, и последующее содержимое будет вставлено непосредственно перед разрывом абзаца.

Когда *node* является блочным узлом, но не [Paragraph](../../paragraph/), курсор перемещается в конец первого абзаца внутри блочного узла, и последующее содержимое будет вставлено непосредственно перед разрывом абзаца.

## Примеры



Показывает, как переместить курсор DocumentBuilder к различным узлам в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте действительную закладку, объект, состоящий из узлов, заключённых между узлом начала закладки,
// и узлом конца закладки.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// Курсор DocumentBuilder всегда находится перед узлом, который мы последним добавили.
// Если курсор builder находится в конце документа, его текущий узел будет null.
// Предыдущий узел — это узел конца закладки, который мы последним добавили.
// Добавление новых узлов с помощью builder будет присоединять их к последнему узлу.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Если мы хотим отредактировать другую часть документа с помощью builder,
// нам понадобится переместить его курсор к узлу, который мы хотим отредактировать.
builder->MoveToBookmark(u"MyBookmark");

// Перемещение его к закладке переместит его к первому узлу внутри начального и конечного узлов закладки, заключённому фрагменту.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// Мы также можем переместить курсор к отдельному узлу следующим образом.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Мы можем использовать специальные методы для перехода к началу/концу документа.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```


Показывает, как переместить позицию курсора [DocumentBuilder](../) к указанному узлу.
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

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
