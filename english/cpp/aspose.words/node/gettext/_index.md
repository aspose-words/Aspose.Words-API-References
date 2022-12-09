---
title: GetText
second_title: Aspose.Words for C++ API Reference
description: Gets the text of this node and of all its children.
type: docs
weight: 183
url: /cpp/aspose.words/node/gettext/
---
## Node::GetText method


Gets the text of this node and of all its children.

```cpp
virtual System::String Aspose::Words::Node::GetText()
```

## Remarks


The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).

## Examples



Shows how to use control characters. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert paragraphs with text with DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Converting the document to text form reveals that control characters
// represent some of the document's structural elements, such as page breaks.
ASSERT_EQ(String::Format(u"Hello world!{0}", ControlChar::Cr()) + String::Format(u"Hello again!{0}", ControlChar::Cr()) + ControlChar::PageBreak(),
          doc->GetText());

// When converting a document to string form,
// we can omit some of the control characters with the Trim method.
ASSERT_EQ(String::Format(u"Hello world!{0}", ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
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

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
