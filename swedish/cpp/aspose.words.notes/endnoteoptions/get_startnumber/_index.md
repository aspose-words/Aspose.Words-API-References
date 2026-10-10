---
title: "Aspose::Words::Notes::EndnoteOptions::get_StartNumber metod"
linktitle: "get_StartNumber"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::EndnoteOptions::get_StartNumber metod. Anger startnumret eller tecknet för den första automatiskt numrerade slutnoten i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.notes/endnoteoptions/get_startnumber/
---
## EndnoteOptions::get_StartNumber method


Anger startnumret eller tecknet för den första automatiskt numrerade slutnoten.

```cpp
int32_t Aspose::Words::Notes::EndnoteOptions::get_StartNumber() override
```

## Anmärkningar


Denna egenskap har endast effekt när [RestartRule](../get_restartrule/) är inställd på [Continuous](../../footnotenumberingrule/).

## Exempel



Visar hur man anger ett tal där dokumentet börjar fotnot-/slutnoträkningen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fotnoter och slutnoter är ett sätt att bifoga en referens eller en sidokommentar till text.
// som inte stör huvudtextens flöde.
// Att infoga en fotnot/slutnot lägger till en liten upphöjd referenssymbol
// i huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnotsposter visas som standard längst ner på varje sida som innehåller
// deras referenssymboler, och slutnoter visas i slutet av dokumentet.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// Som standard är referenssymbolen för varje fotnot och slutnot dess index
// bland alla dokumentets fotnoter/slutnoter. Varje dokument upprätthåller separata räknare
// för fotnoter och för slutnoter, som båda börjar på 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// Vi kan använda egenskapen "StartNumber" för att få dokumentet att
// börja en fotnot- eller slutnoträkning på ett annat tal.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## Se även

* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
