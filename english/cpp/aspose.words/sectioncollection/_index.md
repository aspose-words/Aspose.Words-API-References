---
title: Aspose::Words::SectionCollection class
linktitle: SectionCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::SectionCollection class. A collection of Section objects in the document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 59000
url: /cpp/aspose.words/sectioncollection/
---
## SectionCollection class


A collection of [Section](../section/) objects in the document. To learn more, visit the [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) documentation article.

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](../nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](../nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Retrieves a section at the given index. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all sections from the collection to a new array of sections. |
| static [Type](./type/)() |  |
## Remarks


A Microsoft Word document can contain multiple sections. To create a section in a Microsoft Word, select the Insert/Break command and select a break type. The break specifies whether section starts on a new page or on the same page.

Programmatically inserting and removing sections can be used to customize documents produced during mail merge. If a document needs to have different content or parts of the content depending on some criteria, then you can create a "master" document that contains multiple sections and delete some of the sections before or after mail merge.

## Examples



Shows how to add and remove sections in a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c"
          u"Section 2",
          doc->GetText().Trim());

// Delete the first section from the document.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Append a copy of what is now the first section to the end of the document.
int lastSectionIdx = doc->get_Sections()->get_Count() - 1;
SharedPtr<Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c"
          u"Section 2",
          doc->GetText().Trim());
```

## See Also

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
