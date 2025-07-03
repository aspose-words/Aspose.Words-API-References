---
title: Aspose::Words::Range::get_StructuredDocumentTags method
linktitle: get_StructuredDocumentTags
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Range::get_StructuredDocumentTags method. Returns a StructuredDocumentTags collection that represents all structured document tags in the range in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


Returns a [StructuredDocumentTags](./) collection that represents all structured document tags in the range.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


## Examples



Shows how to remove structured document tag. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> structuredDocumentTags = doc->get_Range()->get_StructuredDocumentTags();
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt;
for (int32_t i = 0; i < structuredDocumentTags->get_Count(); i++)
{
    sdt = structuredDocumentTags->idx_get(i);
    std::cout << sdt->get_Title() << std::endl;
}

sdt = structuredDocumentTags->GetById(1691867797);
ASSERT_EQ(1691867797, sdt->get_Id());

ASSERT_EQ(5, structuredDocumentTags->get_Count());
// Remove the structured document tag by Id.
structuredDocumentTags->Remove(1691867797);
// Remove the structured document tag at position 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## See Also

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
