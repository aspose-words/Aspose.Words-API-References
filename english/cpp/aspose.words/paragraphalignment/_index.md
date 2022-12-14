---
title: ParagraphAlignment
second_title: Aspose.Words for C++ API Reference
description: Specifies text alignment in a paragraph.
type: docs
weight: 1431
url: /cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


Specifies text alignment in a paragraph.

```cpp
enum class ParagraphAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | 0 | Text is aligned to the left. |
| Center | 1 | Text is centered horizontally. |
| Right | 2 | Text is aligned to the right. |
| Justify | 3 | Text is aligned to both left and right. |
| Distributed | 4 | Text is evenly distributed. |
| ArabicMediumKashida | 5 | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ArabicHighKashida | 7 | Arabic only. Kashida length for text is extended to its widest possible length. |
| ArabicLowKashida | 8 | Arabic only. Kashida length for text is extended to a slightly longer length. |
| ThaiDistributed | 9 | Thai only. Text is justified with an optimization for Thai. |
| MathElementCenterAsGroup | 10 | The only [Math](../../aspose.words.math/) element in a line, aligned as 'Centered As Group'. |


## Examples



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
