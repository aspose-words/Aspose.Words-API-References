---
title: Aspose::Words::Layout::RevisionOptions class
linktitle: RevisionOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::RevisionOptions class. Allows to control how document revisions are handled during layout process. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Allows to control how document revisions are handled during layout process. To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) documentation article.

```cpp
class RevisionOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Allows to specify the color to be used for comments. Default value is [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | Allows to specify the color to be used for deleted cells [Deletion](../../aspose.words/revisiontype/). Default value is [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Allows to specify the color to be used for deleted content [Deletion](../../aspose.words/revisiontype/). Default value is [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Allows to specify the effect to be applied to the deleted content [Deletion](../../aspose.words/revisiontype/). Default value is [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | Allows to specify the color to be used for inserted cells [Insertion](../../aspose.words/revisiontype/). Default value is [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Allows to specify the color to be used for inserted content [Insertion](../../aspose.words/revisiontype/). Default value is [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Allows to specify the effect to be applied to the inserted content [Insertion](../../aspose.words/revisiontype/). Default value is [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | Allows to specify the measurement units for revision comments. Default value is [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | Allows to specify the color to be used for areas where content was moved from [Moving](../../aspose.words/revisiontype/). Default value is [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | Allows to specify the effect to be applied to the areas where content was moved from [Moving](../../aspose.words/revisiontype/). Default value is [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | Allows to specify the color to be used for areas where content was moved to [Moving](../../aspose.words/revisiontype/). Default value is [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | Allows to specify the effect to be applied to the areas where content was moved to [Moving](../../aspose.words/revisiontype/). Default value is [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Allows to specify the color to be used for content with changes of formatting properties [FormatChange](../../aspose.words/revisiontype/) Default value is [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Allows to specify the effect for content areas with changes of formatting properties [FormatChange](../../aspose.words/revisiontype/) Default value is [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Gets or sets rendering position of revision bars. Default value is [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Gets or sets width of revision bars, points. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Allows to specify whether the revisions are rendered in the balloons. Default value is [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Allows to specify whether the original text should be shown instead of revised one. Default value is **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Allow to specify whether revision text should be marked with special formatting markup. Default value is **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | Allows to specify the color to be used for deleted cells [Deletion](../../aspose.words/revisiontype/). Default value is [Pink](../revisioncolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | Allows to specify the color to be used for inserted cells [Insertion](../../aspose.words/revisiontype/). Default value is [Blue](../revisioncolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Allows to specify the measurement units for revision comments. Default value is [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Setter for [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Setter for [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

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

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
