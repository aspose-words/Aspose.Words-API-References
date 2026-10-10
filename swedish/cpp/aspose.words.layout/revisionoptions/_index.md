---
title: "Aspose::Words::Layout::RevisionOptions klass"
linktitle: "RevisionOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::RevisionOptions klass. Tillåter att kontrollera hur dokumentrevisioner hanteras under layoutprocessen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Tillåter att kontrollera hur dokumentrevisioner hanteras under layoutprocessen. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class RevisionOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Tillåter att ange färgen som ska användas för kommentarer. Standardvärdet är [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | Tillåter att ange färgen som ska användas för borttagna celler [Deletion](../../aspose.words/revisiontype/). Standardvärdet är [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Tillåter att ange färgen som ska användas för borttaget innehåll [Deletion](../../aspose.words/revisiontype/). Standardvärdet är [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Tillåter att ange effekten som ska tillämpas på det borttagna innehållet [Deletion](../../aspose.words/revisiontype/). Standardvärdet är [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | Tillåter att ange färgen som ska användas för infogade celler [Insertion](../../aspose.words/revisiontype/). Standardvärdet är [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Tillåter att ange färgen som ska användas för infogat innehåll [Insertion](../../aspose.words/revisiontype/). Standardvärdet är [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Tillåter att ange effekten som ska tillämpas på det infogade innehållet [Insertion](../../aspose.words/revisiontype/). Standardvärdet är [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | Tillåter att ange mätenheterna för revisionskommentarer. Standardvärdet är [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | Tillåter att ange färgen som ska användas för områden där innehåll flyttades från [Moving](../../aspose.words/revisiontype/). Standardvärdet är [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | Tillåter att ange effekten som ska tillämpas på områden där innehåll flyttades från [Moving](../../aspose.words/revisiontype/). Standardvärdet är [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | Tillåter att ange färgen som ska användas för områden där innehåll flyttades till [Moving](../../aspose.words/revisiontype/). Standardvärdet är [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | Tillåter att ange effekten som ska tillämpas på områden där innehåll flyttades till [Moving](../../aspose.words/revisiontype/). Standardvärdet är [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Tillåter att ange färgen som ska användas för innehåll med ändringar av formateringsegenskaper [FormatChange](../../aspose.words/revisiontype/) Standardvärdet är [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Tillåter att ange effekten för innehållsområden med ändringar av formateringsegenskaper [FormatChange](../../aspose.words/revisiontype/) Standardvärdet är [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Tillåter att ange färgen som ska användas för sidofält som identifierar dokumentrader som innehåller reviderad information. Standardvärdet är [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Hämtar eller anger renderingsposition för revisionsstaplar. Standardvärdet är [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Hämtar eller anger bredden på revisionsstaplar, punkter. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Tillåter att ange om revisionerna renderas i ballongerna. Standardvärdet är [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Tillåter att ange om den ursprungliga texten ska visas istället för den reviderade. Standardvärdet är **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Tillåter att ange om revisionsstaplar ska renderas nära rader som innehåller reviderat innehåll. Standardvärdet är **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Tillåter att ange om revisionstext ska markeras med speciell formateringsmarkup. Standardvärdet är **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Tillåter att ange mätenheterna för revisionskommentarer. Standardvärdet är [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Sättare för [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

## Exempel



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
