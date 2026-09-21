---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel‑metod"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel‑metod. Anger den maximala rubriknivån där dokumentet ska delas. Standardvärdet är %2 i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Anger den maximala rubriknivån där dokumentet ska delas upp. Standardvärdet är **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Anmärkningar


När [DocumentSplitCriteria](../get_documentsplitcriteria/) inkluderar [HeadingParagraph](../../documentsplitcriteria/) och denna egenskap är satt till ett värde mellan 1 och 9, kommer dokumentet att delas vid stycken formaterade med **Heading 1**, **Heading 2**, **Heading 3** osv. stilar upp till den angivna rubriknivån.

Som standard orsakar endast **Heading 1**- och **Heading 2**‑stycken att dokumentet delas. Att sätta denna egenskap till noll gör att dokumentet inte delas vid rubrikstycken alls.

## Exempel



Visar hur man delar ett utdata‑HTML‑dokument efter rubriker i flera delar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Varje stycke som vi formaterar med en "Heading"‑stil kan fungera som en rubrik.
// Varje rubrik kan också ha en rubriknivå, bestämd av antalet i dess rubrikstil.
// Rubrikerna nedan är på nivåerna 1‑3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Skapa ett HtmlSaveOptions‑objekt och sätt delningskriteriet till "HeadingParagraph".
// Dessa kriterier kommer att dela dokumentet vid stycken med "Heading"‑stilar i flera mindre dokument,
// och spara varje dokument i en separat HTML‑fil i det lokala filsystemet.
// Vi kommer också att sätta den maximala rubriknivån, vilket delar dokumentet till 2.
// När dokumentet sparas kommer det att delas vid rubriker på nivå 1 och 2, men inte på 3 till 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// Vårt dokument har fyra rubriker på nivå 1‑2. En av dessa rubriker kommer inte att vara
// en delningspunkt eftersom den är i början av dokumentet.
// Sparningsoperationen kommer att dela vårt dokument på tre ställen, i fyra mindre dokument.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
