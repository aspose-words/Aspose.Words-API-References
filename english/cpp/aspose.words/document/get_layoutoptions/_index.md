---
title: get_LayoutOptions
second_title: Aspose.Words for C++ API Reference
description: Gets a LayoutOptions object that represents options to control the layout process of this document.
type: docs
weight: 417
url: /cpp/aspose.words/document/get_layoutoptions/
---
## Document.get_LayoutOptions method


Gets a **LayoutOptions** object that represents options to control the layout process of this document.

```cpp
System::SharedPtr<Aspose::Words::Layout::LayoutOptions> Aspose::Words::Document::get_LayoutOptions() const
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


Shows how to hide text in a rendered output document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(ArtifactsDir + u"Document.LayoutOptionsHiddenText.pdf");
```


Shows how to show paragraph marks in a rendered output document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
// with a pilcrow (¶) symbol when we render the document.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(ArtifactsDir + u"Document.LayoutOptionsParagraphMarks.pdf");
```

