---
title: "Aspose::Words::InlineStory::get_StoryType Methode"
linktitle: "get_StoryType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::InlineStory::get_StoryType Methode. Gibt den Typ der Story in C++ zurück."
type: docs
weight: 12000
url: /de/cpp/aspose.words/inlinestory/get_storytype/
---
## InlineStory::get_StoryType method


Gibt den Typ der Geschichte zurück.

```cpp
Aspose::Words::StoryType Aspose::Words::InlineStory::get_StoryType() override=0
```


## Beispiele



Zeigt, wie man [InlineStory](../)-Knoten einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// Tabellenknoten haben eine "EnsureMinimum()"-Methode, die sicherstellt, dass die Tabelle mindestens eine Zelle enthält.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// Wir können eine Tabelle in einer Fußnote platzieren, wodurch sie in der Fußzeile der referenzierenden Seite erscheint.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// Ein InlineStory hat ebenfalls eine "EnsureMinimum()"-Methode, aber in diesem Fall,
// stellt sicher, dass das letzte Kind des Knotens ein Absatz ist,
// damit wir in Microsoft Word leicht klicken und Text schreiben können.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Bearbeiten Sie das Aussehen des Ankers, der die kleine hochgestellte Zahl ist
// im Haupttext, der auf die Fußnote verweist.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// Alle Inline-Story-Knoten haben ihre jeweiligen Story-Typen.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// Ein Kommentar ist ein weiterer Typ einer Inline-Story.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// Der übergeordnete Absatz eines Inline-Story-Knotens ist derjenige aus dem Hauptdokumentkörper.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// Allerdings ist der letzte Absatz derjenige aus dem Kommentar-Textinhalt,
// der sich außerhalb des Hauptdokumentkörpers in einer Sprechblase befindet.
// Ein Kommentar hat standardmäßig keine untergeordneten Knoten,
// so können wir die EnsureMinimum()-Methode anwenden, um hier ebenfalls einen Absatz zu platzieren.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Sobald wir einen Absatz haben, können wir den Builder verschieben, um dies zu tun, und unseren Kommentar schreiben.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## Siehe auch

* Enum [StoryType](../../storytype/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
