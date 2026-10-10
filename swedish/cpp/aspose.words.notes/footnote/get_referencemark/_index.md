---
title: "Aspose::Words::Notes::Footnote::get_ReferenceMark metod"
linktitle: "get_ReferenceMark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::Footnote::get_ReferenceMark metod. Hämtar/sätter anpassad referensmarkering som ska användas för detta fotnot. Standardvärdet är empty string, vilket innebär att automatiskt numrerade fotnoter används i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.notes/footnote/get_referencemark/
---
## Footnote::get_ReferenceMark method


Hämtar/ställer in anpassat referensmärke som ska användas för denna fotnot. Standardvärdet är **empty string**, vilket betyder att automatiskt numrerade fotnoter används.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ReferenceMark() const
```

## Anmärkningar


Om den här egenskapen är inställd på **empty string** eller **null**, så kommer egenskapen [IsAuto](../get_isauto/) automatiskt att sättas till **true**, om den är inställd på något annat så kommer [IsAuto](../get_isauto/) att sättas till **false**.

RTF-format kan bara lagra 1 symbol som anpassad referensmarkering, så vid export kommer endast den första symbolen att skrivas och de övriga kommer att kastas.

## Exempel



Visar hur man infogar och anpassar fotnoter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till text och referera den med en fotnot. Denna fotnot kommer att placera en liten upphöjd referens
// markör efter den text den refererar till och skapa ett post under huvudtexten längst ner på sidan.
// Denna post kommer att innehålla fotnotens referensmarkör och referenstexten,
// vilken vi kommer att skicka till dokumentbyggarens "InsertFootnote"-metod.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Om den här egenskapen är satt till "true", blir vår fotnotens referensmärke
// kommer att vara dess index bland alla sektionens fotnoter.
// Detta är den första fotnoten, så referensmärket blir "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Vi kan flytta dokumentbyggaren in i fotnoten för att redigera dess referenstext.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Vi kan ange ett anpassat referensmärke som fotnoten kommer att använda istället för sitt indexnummer.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Ett bokmärke med flaggan "IsAuto" satt till true kommer fortfarande att visa sitt riktiga index
// även om tidigare bokmärken visar anpassade referensmärken, så blir detta bokmärkes referensmärke ett "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## Se även

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
