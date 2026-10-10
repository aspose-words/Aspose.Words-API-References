---
title: "Aspose::Words::Comment::get_Done-Methode"
linktitle: "get_Done"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment::get_Done-Methode. Liest oder setzt das Flag, das anzeigt, dass der Kommentar als erledigt markiert wurde in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Ermittelt oder setzt das Flag, das anzeigt, dass der Kommentar als erledigt markiert wurde.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## Beispiele



Zeigt, wie man einen Kommentar als "done" markiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Fügen Sie einen Kommentar ein, um einen Fehler hervorzuheben.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Kommentare haben ein "Done"-Flag, das standardmäßig auf "false" gesetzt ist.
// Wenn ein Kommentar vorschlägt, dass wir eine Änderung im Dokument vornehmen,
// Wir können die Änderung anwenden und anschließend das "Done"-Flag setzen, um die Korrektur anzuzeigen.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Kommentare, die "done" sind, unterscheiden sich
// von denen, die nicht "done" sind, durch eine verblasste Textfarbe.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Siehe auch

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
