---
title: "Aspose::Words::InlineStory::get_Tables method"
linktitle: "get_Tables"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::InlineStory::get_Tables method. Hämtar en samling tabeller som är omedelbara barn till berättelsen i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/inlinestory/get_tables/
---
## InlineStory::get_Tables method


Hämtar en samling tabeller som är omedelbara barn till storyn.

```cpp
System::SharedPtr<Aspose::Words::Tables::TableCollection> Aspose::Words::InlineStory::get_Tables() override
```


## Exempel



Visar hur man infogar [InlineStory](../) noder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// Tabellnoder har en "EnsureMinimum()" metod som säkerställer att tabellen har minst en cell.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// Vi kan placera en tabell i en fotnot, vilket får den att visas i sidfoten på den refererande sidan.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// En InlineStory har också en "EnsureMinimum()"-metod, men i detta fall,
// den ser till att det sista barnet i noden är ett stycke,
// så att vi kan klicka och skriva text enkelt i Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Redigera utseendet på ankaret, som är det lilla upphöjda numret
// i huvudtexten som pekar på fotnoten.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// Alla inline‑story‑noder har sina respektive story‑typer.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// En kommentar är en annan typ av inline‑story.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// Den överordnade paragrafen för en inline‑story‑nod kommer att vara den från huvuddokumentets kropp.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// Dock är det sista stycket det som kommer från kommentarens textinnehåll,
// vilket kommer att vara utanför huvuddokumentets kropp i en pratbubbla.
// En kommentar har som standard inga underordnade noder,
// så kan vi använda metoden EnsureMinimum() för att placera ett stycke här också.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// När vi har ett stycke kan vi flytta byggaren för att göra det och skriva vår kommentar.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## Se även

* Class [TableCollection](../../../aspose.words.tables/tablecollection/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
