---
title: "Aspose::Words::DocumentBuilder::MoveToDocumentStart method"
linktitle: "MoveToDocumentStart"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::MoveToDocumentStart. Перемещает курсор в начало документа в C++."
type: docs
weight: 55000
url: /ru/cpp/aspose.words/documentbuilder/movetodocumentstart/
---
## DocumentBuilder::MoveToDocumentStart method


Перемещает курсор в начало документа.

```cpp
void Aspose::Words::DocumentBuilder::MoveToDocumentStart()
```


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

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
