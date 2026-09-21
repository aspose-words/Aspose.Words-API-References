---
title: "Aspose::Words::Notes::FootnoteOptions::get_NumberStyle metod"
linktitle: "get_NumberStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::FootnoteOptions::get_NumberStyle metod. Anger nummerformatet för automatiskt numrerade fotnoter i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.notes/footnoteoptions/get_numberstyle/
---
## FootnoteOptions::get_NumberStyle method


Anger talformatet för automatiskt numrerade fotnoter.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::FootnoteOptions::get_NumberStyle() override
```

## Anmärkningar


Inte alla nummerstilar är tillämpliga för den här egenskapen. För en lista över tillämpliga nummerstilar, se dialogrutan Infoga [Footnote](../../footnote/) eller Slutnot i Microsoft Word. Om du väljer en nummerstil som inte är tillämplig, återgår Microsoft Word till ett standardvärde.

## Exempel



Visar hur man ändrar siffrastilen för fotnot-/slutnotreferensmarkeringar.
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
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// Som standard är referenssymbolen för varje fotnot och slutnot dess index
// bland alla dokumentets fotnoter/slutnoter. Varje dokument upprätthåller separata räknare
// för fotnoter och för slutnoter. Som standard visar fotnoter sina nummer med arabiska siffror,
// och slutnoter visar sina nummer i gemena romerska siffror.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// Vi kan använda egenskapen "NumberStyle" för att tillämpa anpassade numreringsstilar på fotnoter och slutnoter.
// Detta kommer inte att påverka fotnoter/slutnoter med anpassade referensmarkeringar.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```

## Se även

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
