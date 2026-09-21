---
title: "Aspose::Words::Notes::FootnoteNumberingRule enum"
linktitle: "FootnoteNumberingRule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::FootnoteNumberingRule enum. Bestämmer när automatisk fotnot- eller slutnotnumrering startas om i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enum


Bestämmer när automatisk fotnot- eller slutnotnumrering startas om.

```cpp
enum class FootnoteNumberingRule
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Continuous | 0 | Numrering är kontinuerlig genom hela dokumentet. |
| RestartSection | 1 | Numrering startas om vid varje sektion. |
| RestartPage | 2 | Numrering startas om på varje sida. Giltig endast för fotnoter. |
| Default | n/a | Lika med [Continuous](./). |


## Exempel



Visar hur man startar om numreringen av fotnoter/slutnoter på vissa ställen i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fotnoter och slutnoter är ett sätt att bifoga en referens eller en sidokommentar till text.
// som inte stör huvudtextens flöde.
// Att infoga en fotnot/slutnot lägger till en liten upphöjd referenssymbol
// i huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol som matchar referensen
// symbol i huvudtexten. Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnotsposter visas som standard längst ner på varje sida som innehåller
// deras referenssymboler, och slutnoter visas i slutet av dokumentet.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// Som standard är referenssymbolen för varje fotnot och slutnot dess index
// bland alla dokumentets fotnoter/slutnoter. Varje dokument upprätthåller separata räknare
// för fotnoter och slutnoter och återställer inte dessa räknare någonstans.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// Vi kan använda egenskapen "RestartRule" för att få dokumentet att starta om
// fotnot-/slutnoträkningarna på en ny sida eller sektion.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```

## Se även

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
