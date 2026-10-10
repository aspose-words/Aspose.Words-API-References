---
title: "Aspose::Words::DocumentBuilder::get_IsAtEndOfParagraph metod"
linktitle: "get_IsAtEndOfParagraph"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::get_IsAtEndOfParagraph metod. Returnerar true om markören är i slutet av det aktuella stycket i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words/documentbuilder/get_isatendofparagraph/
---
## DocumentBuilder::get_IsAtEndOfParagraph method


Returnerar **true** om markören är i slutet av det aktuella stycket.

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtEndOfParagraph()
```


## Exempel



Visar hur man flyttar en dokumentbyggares markör till olika noder i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett giltigt bokmärke, en entitet som består av noder omslutna av en bokmärkesstartnod,
// och en bokmärkesslutnod.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// Dokumentbyggarens markör är alltid före den nod som vi senast lade till med den.
// Om byggarens markör är i slutet av dokumentet kommer dess aktuella nod att vara null.
// Den föregående noden är bokmärkesslutnoden som vi senast lade till.
// Att lägga till nya noder med byggaren kommer att bifoga dem till den sista noden.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Om vi vill redigera en annan del av dokumentet med byggaren,
// behöver vi flytta dess markör till den nod vi vill redigera.
builder->MoveToBookmark(u"MyBookmark");

// Att flytta den till ett bokmärke kommer att flytta den till den första noden inom bokmärkesstart- och slutnoderna, den omslutna körningen.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// Vi kan också flytta markören till en enskild nod på detta sätt.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Vi kan använda specifika metoder för att flytta till början/slutet av ett dokument.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
