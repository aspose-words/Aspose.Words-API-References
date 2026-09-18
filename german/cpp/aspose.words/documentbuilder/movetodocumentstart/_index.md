---
title: "Aspose::Words::DocumentBuilder::MoveToDocumentStart Methode"
linktitle: "MoveToDocumentStart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToDocumentStart Methode. Bewegt den Cursor zum Anfang des Dokuments in C++."
type: docs
weight: 55000
url: /de/cpp/aspose.words/documentbuilder/movetodocumentstart/
---
## DocumentBuilder::MoveToDocumentStart method


Bewegt den Cursor zum Anfang des Dokuments.

```cpp
void Aspose::Words::DocumentBuilder::MoveToDocumentStart()
```


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
