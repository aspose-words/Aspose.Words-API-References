---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "FootnoteType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::FootnoteType enum. Anger om detta är en fotnot eller en slutnot i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


Anger om detta är en fotnot eller en slutnot.

```cpp
enum class FootnoteType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Footnote | 0 | Objektet är en fotnot. |
| Endnote | 1 | Objektet är en slutnot. |

## Anmärkningar


Både fotnoter och slutnoter representeras av objekt av klassen [Footnote](./). Använd [FootnoteType](../footnote/get_footnotetype/) för att särskilja fotnoter och slutnoter.

## Exempel



Visar hur man refererar text med en fotnot och en slutnot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga lite text och markera den med en fotnot där egenskapen IsAuto är inställd på "true" som standard,
// så att markören som ses i brödtexten automatiskt numreras till "1",
// och fotnoten kommer att visas längst ner på sidan.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Infoga mer text och markera den med en slutnot med en anpassad referensmarkör,
// som kommer att användas i stället för siffran "2" och sätta "IsAuto" till false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Fotnoter visas alltid längst ner på den text de refererar till,
// så att detta sidbrytning inte påverkar fotnoten.
// Å andra sidan är slutnoter alltid i slutet av dokumentet
// så att detta sidbrytning skjuter slutnoten ner till nästa sida.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
