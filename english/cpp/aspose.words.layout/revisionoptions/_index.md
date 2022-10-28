---
title: RevisionOptions
second_title: Aspose.Words for C++ API Reference
description: Allows to control how document revisions are handled during layout process.
type: docs
weight: 53
url: /cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Allows to control how document revisions are handled during layout process.

```cpp
class RevisionOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Allows to specify the color to be used for comments. Default value is **Red**. |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Allows to specify the color to be used for deleted content **Deletion**. Default value is **ByAuthor**. |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Allows to specify the effect to be applied to the deleted content **Deletion**. Default value is **StrikeThrough** |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Allows to specify the color to be used for inserted content **Insertion**. Default value is **ByAuthor**. |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Allows to specify the effect to be applied to the inserted content **Insertion**. Default value is **Underline**. |
| [get_MeasurementUnit](./get_measurementunit/)() const | Allows to specify the measurement units for revision comments. Default value is **Centimeters** |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | Allows to specify the color to be used for areas where content was moved from **Moving**. Default value is **ByAuthor**. |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | Allows to specify the effect to be applied to the areas where content was moved from **Moving**. Default value is **DoubleStrikeThrough** |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | Allows to specify the color to be used for areas where content was moved to **Moving**. Default value is **ByAuthor**. |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | Allows to specify the effect to be applied to the areas where content was moved to **Moving**. Default value is **DoubleUnderline** |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Allows to specify the color to be used for content with changes of formatting properties **FormatChange** Default value is **NoHighlight**. |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Allows to specify the effect for content areas with changes of formatting properties **FormatChange** Default value is **None** |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is **Red**. |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Gets rendering position of revision bars. Default value is **Outside**. |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Gets or sets width of revision bars, points. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Allows to specify whether the revisions are rendered in the balloons. Default value is **None**. |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Allows to specify whether the original text should be shown instead of revised one. Default value is False. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is True. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Allow to specify whether revision text should be marked with special formatting markup. Default value is True. |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Allows to specify the measurement units for revision comments. Default value is **Centimeters** |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Sets rendering position of revision bars. Default value is **Outside**. |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |

## Examples




Shows how to alter the appearance of revisions in a rendered output document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a revision, then change the color of all revisions to green.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Remove the bar that appears to the left of every revised line.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);

doc->Save(ArtifactsDir + u"Document.LayoutOptionsRevisions.pdf");
```

