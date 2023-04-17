---
title: Aspose::Words::Layout::LayoutOptions::get_RevisionOptions method
linktitle: get_RevisionOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutOptions::get_RevisionOptions method. Gets revision options in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.layout/layoutoptions/get_revisionoptions/
---
## LayoutOptions::get_RevisionOptions method


Gets revision options.

```cpp
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> Aspose::Words::Layout::LayoutOptions::get_RevisionOptions() const
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

## See Also

* Class [RevisionOptions](../../revisionoptions/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
