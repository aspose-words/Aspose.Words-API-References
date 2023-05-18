---
title: Aspose::Words::NodeCollection::RemoveAt method
linktitle: RemoveAt
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection::RemoveAt method. Removes the node at the specified index from the collection and from the document in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Removes the node at the specified index from the collection and from the document.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |

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

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
