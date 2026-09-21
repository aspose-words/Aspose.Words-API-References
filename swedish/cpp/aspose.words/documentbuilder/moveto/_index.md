---
title: "Aspose::Words::DocumentBuilder::MoveTo‑metod"
linktitle: "MoveTo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveTo‑metod. Flyttar markören till en inline‑nod eller till slutet av ett stycke i C++."
type: docs
weight: 51000
url: /sv/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


Flyttar markören till en inline-nod eller till slutet av ett stycke.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| nod | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden måste vara ett stycke eller ett direkt barn till ett stycke. |
## Anmärkningar


När *node* är en inline‑nivånod, flyttas markören till den noden och ytterligare innehåll kommer att infogas före den noden.

När *node* är ett [Paragraph](../../paragraph/), flyttas markören till slutet av stycket och ytterligare innehåll kommer att infogas precis före styckebrytningen.

När *node* är en blocknivånod men inte ett [Paragraph](../../paragraph/), flyttas markören till slutet av det första stycket i blocknivånod och ytterligare innehåll kommer att infogas precis före styckebrytningen.

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


Visar hur man flyttar en [DocumentBuilder](../)s markörposition till en angiven nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Dokumentbyggaren har en markör, som fungerar som en del av dokumentet
// där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
// Denna markör fungerar på samma sätt som Microsoft Words blinkande markör,
// och den hamnar också alltid omedelbart efter vilken nod som helst som byggaren just har infogat.
// För att lägga till innehåll i en annan del av dokumentet,
// kan vi flytta markören till en annan nod med metoden "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// Markören är nu framför den nod vi flyttade den till.
// Att lägga till en andra körning kommer att infoga den framför den första körningen.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Flytta markören till slutet av dokumentet för att fortsätta lägga till text i slutet som tidigare.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Se även

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
