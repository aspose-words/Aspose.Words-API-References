---
title: "Aspose::Words::Comment::SetText-Methode"
linktitle: "SetText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment::SetText-Methode. Dies ist eine Komfortmethode, die es ermöglicht, den Text des Kommentars in C++ einfach festzulegen."
type: docs
weight: 22000
url: /de/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


Dies ist eine Komfortmethode, die das einfache Festlegen des Textes des Kommentars ermöglicht.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Text | const System::String\& | Der neue Text des Kommentars. |
## Hinweise


Diese Methode ermöglicht es, den Text eines Kommentars schnell aus einer Zeichenkette festzulegen. Die Zeichenkette kann Absatzumbrüche enthalten, wodurch entsprechend Absätze im Kommentar erstellt werden. Wenn Sie komplexere Elemente in den Kommentar einfügen möchten, zum Beispiel Lesezeichen oder Tabellen oder eine Rich-Formatierung anwenden, müssen Sie die entsprechenden Node‑Klassen verwenden, um den Kommentartext aufzubauen.

## Beispiele



Zeigt, wie man einem Dokument einen Kommentar hinzufügt und darauf antwortet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Platziere den Kommentar an einem Knoten im Dokumentenkörper.
// Dieser Kommentar wird an der Position seines Absatzes angezeigt,
// außerhalb des rechten Seitenrandes und mit einer gepunkteten Linie, die ihn mit seinem Absatz verbindet.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Füge eine Antwort hinzu, die unter dem übergeordneten Kommentar angezeigt wird.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Kommentare und Antworten sind beide Comment‑Knoten.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Kommentare, die nicht auf andere Kommentare antworten, sind "Top‑Level". Sie haben keine übergeordneten Kommentare.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Antworten haben einen übergeordneten Top‑Level‑Kommentar.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## Siehe auch

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
