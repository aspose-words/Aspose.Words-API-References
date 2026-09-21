---
title: "Aspose::Words::Layout::LayoutOptions-klass"
linktitle: "LayoutOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutOptions-klass. Innehåller alternativ som möjliggör styrning av dokumentlayoutprocessen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Innehåller de alternativ som möjliggör styrning av dokumentlayoutprocessen. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Callback](./get_callback/)() const | Hämtar [IPageLayoutCallback](../ipagelayoutcallback/) implementationen som används av sidlayoutmodellen. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Hämtar eller sätter hur kommentarer renderas. Standardvärdet är [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Hämtar eller sätter beteendemodet för beräkning av sidnummer när ett kontinuerligt avsnitt startar om sidnumreringen. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | Hämtar eller sätter indikation på om kompatibilitetsalternativet "Use printer metrics to lay out document" ignoreras. Standard är **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | Hämtar eller sätter en indikation på om de ursprungliga teckensnittsmåtten ska användas efter teckensnittssubstitution. Standard är **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Hämtar revisionsalternativ. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Hämtar eller sätter indikation på om dold text i dokumentet renderas. Standard är **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Hämtar eller sätter indikation på om stycketecken renderas. Standard är **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Hämtar [ITextShaperFactory](../) implementationen som används för avancerade typografifunktioner. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Sätter [IPageLayoutCallback](../ipagelayoutcallback/) implementationen som används av sidlayoutmodellen. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Sättare för [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Sättare för [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Sättare för [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | Sättare för [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Sättare för [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Inställare för [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Ställer in [ITextShaperFactory](../) implementation som används för avancerade typografifunktioner vid rendering. |
| static [Type](./type/)() |  |
## Anmärkningar


Du skapar inte instanser av den här klassen direkt. Använd egenskapen [LayoutOptions](../../aspose.words/document/get_layoutoptions/) för att komma åt layoutalternativ för detta dokument.

Observera att efter att ha ändrat någon av alternativen i den här klassen bör metoden [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) anropas för att de ändrade alternativen ska tillämpas på layouten.

## Exempel



Visar hur man döljer text i ett renderat utdata-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga dold text och ange sedan om vi vill utesluta den från ett renderat dokument.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Visar hur man visar stycketecken i ett renderat utdata-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till några stycken och aktivera sedan stycketecken för att visa slutet på styckena
// med ett pilcrow‑symbol (¶) när vi renderar dokumentet.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Visar hur man ändrar utseendet på revisioner i ett renderat utdata-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en revision och ändra sedan färgen på alla revisioner till grön.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Ta bort stapeln som visas till vänster om varje reviderad rad.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Se även

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
