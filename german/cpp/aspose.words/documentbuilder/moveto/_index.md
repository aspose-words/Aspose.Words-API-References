---
title: "Aspose::Words::DocumentBuilder::MoveTo Methode"
linktitle: "MoveTo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveTo Methode. Verschiebt den Cursor zu einem Inline-Knoten oder zum Ende eines Absatzes in C++."
type: docs
weight: 51000
url: /de/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


Bewegt den Cursor zu einem Inline‑Knoten oder zum Ende eines Absatzes.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Knoten | const System::SharedPtr\<Aspose::Words::Node\>\& | Der Knoten muss ein Absatz oder ein direktes Kind eines Absatzes sein. |
## Hinweise


Wenn *node* ein Inline-Level-Knoten ist, wird der Cursor zu diesem Knoten verschoben und weiterer Inhalt wird vor diesem Knoten eingefügt.

Wenn *node* ein [Paragraph](../../paragraph/) ist, wird der Cursor zum Ende des Absatzes verschoben und weiterer Inhalt wird unmittelbar vor dem Absatzumbruch eingefügt.

Wenn *node* ein Block-Level-Knoten ist, aber kein [Paragraph](../../paragraph/), wird der Cursor zum Ende des ersten Absatzes im Block-Level-Knoten verschoben und weiterer Inhalt wird unmittelbar vor dem Absatzumbruch eingefügt.

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


Zeigt, wie man die Cursorposition eines [DocumentBuilder](../) zu einem angegebenen Knoten verschiebt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Der Dokument-Builder hat einen Cursor, der als Teil des Dokuments fungiert
// wo der Builder neue Knoten anhängt, wenn wir seine Dokumentenkonstruktionsmethoden verwenden.
// Dieser Cursor funktioniert auf dieselbe Weise wie der blinkende Cursor von Microsoft Word,
// und er endet außerdem immer sofort nach jedem Knoten, den der Builder gerade eingefügt hat.
// Um Inhalte an einem anderen Teil des Dokuments anzufügen,
// können wir den Cursor mit der "MoveTo"-Methode zu einem anderen Knoten bewegen.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// Der Cursor befindet sich jetzt vor dem Knoten, zu dem wir ihn verschoben haben.
// Das Hinzufügen eines zweiten Runs fügt ihn vor dem ersten Run ein.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Bewege den Cursor ans Ende des Dokuments, um das Anfügen von Text am Ende wie zuvor fortzusetzen.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Siehe auch

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
