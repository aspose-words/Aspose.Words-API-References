---
title: LayoutOptions
second_title: Aspose.Words for C++ API Reference
description: Holds the options that allow controlling the document layout process.
type: docs
weight: 27
url: /cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Holds the options that allow controlling the document layout process.

```cpp
class LayoutOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Callback](./get_callback/)() const | Gets [IPageLayoutCallback](../ipagelayoutcallback/) implementation used by page layout model. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Gets or sets the way comments are rendered. Default value is **ShowInBalloons**. |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is True. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Gets revision options. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Gets or sets indication of whether hidden text in the document is rendered. Default is False. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Gets or sets indication of whether paragraph marks are rendered. Default is False. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Gets **ITextShaperFactory** implementation used for Advanced Typography rendering features. |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Sets [IPageLayoutCallback](../ipagelayoutcallback/) implementation used by page layout model. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Setter for [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Setter for [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Setter for [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Setter for [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Setter for [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Sets **ITextShaperFactory** implementation used for Advanced Typography rendering features. |

You do not create instances of this class directly. Use the [LayoutOptions](../../aspose.words/document/get_layoutoptions/) property to access layout options for this document.

Note that after changing any of the options present in this class, [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) method should be called in order for the changed options to be applied to the layout.

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

