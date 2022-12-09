---
title: AppendChild
second_title: Aspose.Words for C++ API Reference
description: Adds the specified node to the end of the list of child nodes for this node.
type: docs
weight: 14
url: /cpp/aspose.words/compositenode/appendchild/
---
## CompositeNode::AppendChild method


Adds the specified node to the end of the list of child nodes for this node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::AppendChild(const System::SharedPtr<Aspose::Words::Node> &newChild)
```


| Parameter | Type | Description |
| --- | --- | --- |
| newChild | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to add. |

### ReturnValue

The node added.
## Remarks


If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [ImportNode()](../) to import the node to the current document. The imported node can then be inserted into the current document.

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

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
