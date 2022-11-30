---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Retrieves a section at the given index.
type: docs
weight: 1
url: /cpp/aspose.words/sectioncollection/idx_get/
---
## SectionCollection::idx_get method


Retrieves a section at the given index.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::SectionCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the list of sections. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples



Shows when to recalculate the page layout of the document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Saving a document to PDF, to an image, or printing for the first time will automatically
// cache the layout of the document within its pages.
doc->Save(ArtifactsDir + u"Document.UpdatePageLayout.1.pdf");

// Modify the document in some way.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Orientation::Landscape);

// In the current version of Aspose.Words, modifying the document does not automatically rebuild
// the cached page layout. If we wish for the cached layout
// to stay up to date, we will need to update it manually.
doc->UpdatePageLayout();

doc->Save(ArtifactsDir + u"Document.UpdatePageLayout.2.pdf");
```


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

## See Also

* Class [Section](../../section/)
* Class [SectionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
