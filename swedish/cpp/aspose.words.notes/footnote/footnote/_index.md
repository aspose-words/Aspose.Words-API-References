---
title: "Aspose::Words::Notes::Footnote::Footnote konstruktor"
linktitle: "Footnote"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::Footnote::Footnote konstruktor. Initierar en instans av Footnote‑klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.notes/footnote/footnote/
---
## Footnote::Footnote constructor


Initierar en instans av klassen [Footnote](../).

```cpp
Aspose::Words::Notes::Footnote::Footnote(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Notes::FootnoteType footnoteType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
| footnoteType | Aspose::Words::Notes::FootnoteType | Ett [FootnoteType](../get_footnotetype/) värde som anger om detta är en fotnot eller slutnot. |
## Anmärkningar


När [Footnote](../) skapas, tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../../aspose.words/node/get_parentnode/) är **null**.

För att lägga till [Footnote](../) i dokumentet, använd[InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) på det stycke där du vill att fotnoten ska infogas.

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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
