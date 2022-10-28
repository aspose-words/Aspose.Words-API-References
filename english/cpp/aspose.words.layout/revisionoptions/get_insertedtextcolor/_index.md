---
title: get_InsertedTextColor
second_title: Aspose.Words for C++ API Reference
description: Allows to specify the color to be used for inserted content Insertion. Default value is ByAuthor.
type: docs
weight: 40
url: /cpp/aspose.words.layout/revisionoptions/get_insertedtextcolor/
---
## RevisionOptions.get_InsertedTextColor method


Allows to specify the color to be used for inserted content **Insertion**. Default value is **ByAuthor**.

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor()
```


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

