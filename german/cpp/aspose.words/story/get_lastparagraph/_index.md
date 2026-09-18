---
title: "Aspose::Words::Story::get_LastParagraph Methode"
linktitle: "get_LastParagraph"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Story::get_LastParagraph Methode. Gibt den letzten Absatz der Story in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Ermittelt den letzten Absatz in der Geschichte.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## Beispiele



Zeigt, wie man die Cursorposition eines [DocumentBuilder](../../documentbuilder/) zu einem angegebenen Knoten verschiebt.
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

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
