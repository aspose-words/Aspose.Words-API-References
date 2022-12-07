---
title: Delete
second_title: Aspose.Words for C++ API Reference
description: Deletes all characters of the range.
type: docs
weight: 14
url: /cpp/aspose.words/range/delete/
---
## Range::Delete method


Deletes all characters of the range.

```cpp
void Aspose::Words::Range::Delete()
```


## Examples



Shows how to delete all the nodes from a range. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add text to the first section in the document, and then add another section.
builder->Write(u"Section 1. ");
builder->InsertBreak(BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Remove the first section entirely by removing all the nodes
// within its range, including the section itself.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## See Also

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
