---
title: Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition method
linktitle: get_RevisionBarsPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition method. Gets or sets rendering position of revision bars. Default value is Outside in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.layout/revisionoptions/get_revisionbarsposition/
---
## RevisionOptions::get_RevisionBarsPosition method


Gets or sets rendering position of revision bars. Default value is [Outside](../../../aspose.words.drawing/horizontalalignment/).

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition() const
```


## Examples



Shows how to alter the appearance of revisions in a rendered output document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a revision, then change the color of all revisions to green.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Remove the bar that appears to the left of every revised line.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## See Also

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
