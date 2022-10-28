---
title: EnsureMinimum
second_title: Aspose.Words for C++ API Reference
description: Ensures that the section has Body with one Paragraph.
type: docs
weight: 92
url: /cpp/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method


Ensures that the section has [Body](../../body/) with one [Paragraph](../../paragraph/).

```cpp
void Aspose::Words::Section::EnsureMinimum()
```


## Examples




Shows how to prepare a new section node for editing. 
```cpp
auto doc = MakeObject<Document>();

// A blank document comes with a section, which has a body, which in turn has a paragraph.
// We can add contents to this document by adding elements such as text runs, shapes, or tables to that paragraph.
ASSERT_EQ(NodeType::Section, doc->GetChild(NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(NodeType::Any, 0, true)->get_NodeType());

// If we add a new section like this, it will not have a body, or any other child nodes.
doc->get_Sections()->Add(MakeObject<Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(NodeType::Any, true)->get_Count());

// Run the "EnsureMinimum" method to add a body and a paragraph to this section to begin editing it.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

