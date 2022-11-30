---
title: get_Body
second_title: Aspose.Words for C++ API Reference
description: Returns the Body child node of the section.
type: docs
weight: 105
url: /cpp/aspose.words/section/get_body/
---
## Section::get_Body method


Returns the **Body** child node of the section.

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## Remarks


**Body** contains main text of the section.

Returns null if the section does not have a **Body** node among its children.

## Examples



Clears main text from all sections from the document leaving the sections themselves. 
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

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = MakeObject<Body>(doc);
section->AppendChild(body);

// This body has no children, so we cannot add runs to it yet.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(NodeType::Any, true)->get_Count());

// Call the "EnsureMinimum" to make sure that this body contains at least one empty paragraph.
body->EnsureMinimum();

// Now, we can add runs to the body, and get the document to display them.
body->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
