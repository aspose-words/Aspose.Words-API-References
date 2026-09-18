---
title: "Aspose::Words::DocumentBuilder::MoveToBookmark Methode"
linktitle: "MoveToBookmark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToBookmark Methode. Verschiebt den Cursor zu einem Lesezeichen in C++."
type: docs
weight: 52000
url: /de/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


Bewegt den Cursor zu einem Lesezeichen.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | const System::String\& | Der Name des Lesezeichens, zu dem der Cursor verschoben werden soll. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Hinweise


Verschiebt den Cursor zu einer Position direkt nach dem Beginn des Lesezeichens mit dem angegebenen Namen.

Der Vergleich ist nicht groß-/kleinschreibungssensitiv. Wenn das Lesezeichen nicht gefunden wurde, wird **false** zurückgegeben und der Cursor wird nicht verschoben.

Das Einfügen neuen Textes ersetzt nicht den vorhandenen Text des Lesezeichens.

Beachten Sie, dass einige Lesezeichen im Dokument Formularfeldern zugeordnet sind. Das Verschieben zu einem solchen Lesezeichen und das Einfügen von Text dort fügt den Text in den Code des Formularfeldes ein. Obwohl dies das Formularfeld nicht ungültig macht, wird der eingefügte Text nicht sichtbar sein, weil er Teil des Feldcodes wird.

## Beispiele



Zeigt, wie der Cursor eines DocumentBuilders zu verschiedenen Knoten in einem Dokument bewegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie ein gültiges Lesezeichen, ein Objekt, das aus Knoten besteht, die von einem Lesezeichen‑Startknoten umschlossen werden,
// und einem Lesezeichen‑Endknoten.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// Der Cursor des DocumentBuilders steht immer vor dem Knoten, den wir zuletzt damit hinzugefügt haben.
// Wenn der Cursor des Builders am Ende des Dokuments steht, ist sein aktueller Knoten null.
// Der vorherige Knoten ist der Lesezeichen‑Endknoten, den wir zuletzt hinzugefügt haben.
// Das Hinzufügen neuer Knoten mit dem Builder wird sie an den letzten Knoten anhängen.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Wenn wir mit dem Builder einen anderen Teil des Dokuments bearbeiten möchten,
// müssen wir seinen Cursor zu dem Knoten bringen, den wir bearbeiten wollen.
builder->MoveToBookmark(u"MyBookmark");

// Das Verschieben zu einem Lesezeichen führt dazu, dass es zum ersten Knoten innerhalb der Lesezeichen‑Start- und Endknoten, dem eingeschlossenen Lauf, bewegt wird.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// Wir können den Cursor auch zu einem einzelnen Knoten wie folgt bewegen.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Wir können spezifische Methoden verwenden, um zum Anfang/Ende eines Dokuments zu springen.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


Bewegt den Cursor zu einem Lesezeichen mit höherer Präzision.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | const System::String\& | Der Name des Lesezeichens, zu dem der Cursor verschoben werden soll. |
| isStart | bool | Wenn **true**, wird der Cursor zum Anfang des Lesezeichens verschoben. Wenn **false**, wird der Cursor zum Ende des Lesezeichens verschoben. |
| isAfter | bool | Wenn **true**, wird der Cursor nach der Start- oder Endposition des Lesezeichens verschoben. Wenn **false**, wird der Cursor vor der Start- oder Endposition des Lesezeichens verschoben. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Hinweise


Verschiebt den Cursor zu einer Position vor oder nach dem Start oder Ende des Lesezeichens.

Wenn die gewünschte Position nicht auf Inline-Ebene liegt, wird zum nächsten Absatz verschoben.

Der Vergleich ist nicht groß-/kleinschreibungssensitiv. Wenn das Lesezeichen nicht gefunden wurde, wird **false** zurückgegeben und der Cursor wird nicht verschoben.

## Beispiele



Zeigt, wie man den Einfügepunkt‑Cursor eines DocumentBuilder‑Knotens zu einem Lesezeichen verschiebt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ein gültiges Lesezeichen besteht aus einem BookmarkStart‑Knoten, einem BookmarkEnd‑Knoten mit einem
// passendem Lesezeichennamen irgendwo danach und Inhalten, die von diesen Knoten umschlossen werden.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// Es gibt 4 Möglichkeiten, den Cursor eines DocumentBuilder zu einem Lesezeichen zu bewegen.
// Wenn wir zwischen den BookmarkStart‑ und BookmarkEnd‑Knoten liegen, befindet sich der Cursor innerhalb des Lesezeichens.
// Das bedeutet, dass jeder vom Builder hinzugefügte Text Teil des Lesezeichens wird.
// 1 -  Außerhalb des Lesezeichens, vor dem BookmarkStart‑Knoten:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  Innerhalb des Lesezeichens, direkt nach dem BookmarkStart‑Knoten:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  Innerhalb des Lesezeichens, direkt vor dem BookmarkEnd‑Knoten:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  Außerhalb des Lesezeichens, nach dem BookmarkEnd‑Knoten:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
