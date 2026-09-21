---
title: "Aspose::Words::DocumentBuilder::MoveToBookmark metod"
linktitle: "MoveToBookmark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToBookmark metod. Flyttar markören till ett bokmärke i C++."
type: docs
weight: 52000
url: /sv/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


Flyttar markören till ett bokmärke.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | const System::String\& | Namnet på bokmärket att flytta markören till. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Anmärkningar


Flyttar markören till en position precis efter början av bokmärket med det angivna namnet.

Jämförelsen är inte skiftlägeskänslig. Om bokmärket inte hittas returneras **false** och markören flyttas inte.

Att infoga ny text ersätter inte befintlig text i bokmärket.

Observera att vissa bokmärken i dokumentet är tilldelade formulärfält. Att flytta till ett sådant bokmärke och infoga text där placerar texten i formulärfältets kod. Även om detta inte ogiltigförklarar formulärfältet, kommer den infogade texten inte att vara synlig eftersom den blir en del av fältkoden.

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
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


Flyttar markören till ett bokmärke med högre precision.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | const System::String\& | Namnet på bokmärket att flytta markören till. |
| isStart | bool | När **true** flyttas markören till början av bokmärket. När **false** flyttas markören till slutet av bokmärket. |
| isAfter | bool | När **true** flyttas markören till att vara efter bokmärkets start‑ eller slutposition. När **false** flyttas markören till att vara före bokmärkets start‑ eller slutposition. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Anmärkningar


Flyttar markören till en position före eller efter bokmärkets start eller slut.

Om önskad position inte är på inline‑nivå flyttas den till nästa stycke.

Jämförelsen är inte skiftlägeskänslig. Om bokmärket inte hittas returneras **false** och markören flyttas inte.

## Exempel



Visar hur man flyttar dokumentbyggarens nodinfogningspunkt‑markör till ett bokmärke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett giltigt bokmärke består av en BookmarkStart‑nod, en BookmarkEnd‑nod med en
// matchande bokmärkesnamn någonstans efteråt, samt innehåll som omsluts av dessa noder.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// Det finns 4 sätt att flytta dokumentbyggarens markör till ett bokmärke.
// Om vi befinner oss mellan BookmarkStart‑ och BookmarkEnd‑noderna kommer markören att vara inne i bokmärket.
// Detta innebär att all text som läggs till av byggaren blir en del av bokmärket.
// 1 -  Utanför bokmärket, framför BookmarkStart‑nod:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  Inuti bokmärket, precis efter BookmarkStart-noden:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  Inuti bokmärket, precis framför BookmarkEnd-noden:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  Utanför bokmärket, efter BookmarkEnd-noden:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
