---
title: PaperSize
second_title: Aspose.Words for C++ API Reference
description: Specifies paper size.
type: docs
weight: 1405
url: /cpp/aspose.words/papersize/
---
## PaperSize enum


Specifies paper size.

```cpp
enum class PaperSize
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| A3 | 0 | 297 x 420 mm. |
| A4 | 1 | 210 x 297 mm. |
| A5 | 2 | 148 x 210 mm. |
| B4 | 3 | 250 x 353 mm. |
| B5 | 4 | 176 x 250 mm. |
| Executive | 5 | 7.25 x 10.5 inches. |
| Folio | 6 | 8.5 x 13 inches. |
| Ledger | 7 | 17 x 11 inches. |
| Legal | 8 | 8.5 x 14 inches. |
| Letter | 9 | 8.5 x 11 inches. |
| EnvelopeDL | 10 | 110 x 220 mm. |
| Quarto | 11 | 8.47 x 10.83 inches. |
| Statement | 12 | 8.5 x 5.5 inches. |
| Tabloid | 13 | 11 x 17 inches. |
| Paper10x14 | 14 | 10 x 14 inches. |
| Paper11x17 | 15 | 11 x 17 inches. |
| Number10Envelope | 16 | 4.125 x 9.5 inches. |
| Custom | 17 | Custom paper size. |


## Examples



Shows how to adjust paper size, orientation, margins, along with other settings for a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(ArtifactsDir + u"PageSetup.PageMargins.docx");
```


Shows how to set page sizes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// We can change the current page's size to a pre-defined size
// by using the "PaperSize" property of this section's PageSetup object.
builder->get_PageSetup()->set_PaperSize(PaperSize::Tabloid);

ASPOSE_ASSERT_EQ(792.0, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(1224.0, builder->get_PageSetup()->get_PageHeight());

builder->Writeln(String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

// Each section has its own PageSetup object. When we use a document builder to make a new section,
// that section's PageSetup object inherits all the previous section's PageSetup object's values.
builder->InsertBreak(BreakType::SectionBreakEvenPage);

ASSERT_EQ(PaperSize::Tabloid, builder->get_PageSetup()->get_PaperSize());

builder->get_PageSetup()->set_PaperSize(PaperSize::A5);
builder->Writeln(String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

ASPOSE_ASSERT_EQ(419.55, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(595.30, builder->get_PageSetup()->get_PageHeight());

builder->InsertBreak(BreakType::SectionBreakEvenPage);

// Set a custom size for this section's pages.
builder->get_PageSetup()->set_PageWidth(620);
builder->get_PageSetup()->set_PageHeight(480);

ASSERT_EQ(PaperSize::Custom, builder->get_PageSetup()->get_PaperSize());

builder->Writeln(String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

doc->Save(ArtifactsDir + u"PageSetup.PaperSizes.docx");
```


Shows how to construct an Aspose.Words document by hand. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc->RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
auto section = MakeObject<Section>(doc);
doc->AppendChild(section);

// Set some page setup properties for the section.
section->get_PageSetup()->set_SectionStart(SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(PaperSize::Letter);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = MakeObject<Body>(doc);
section->AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
auto para = MakeObject<Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

body->AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
auto run = MakeObject<Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(ArtifactsDir + u"Section.CreateManually.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
