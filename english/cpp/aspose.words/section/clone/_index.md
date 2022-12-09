---
title: Clone
second_title: Aspose.Words for C++ API Reference
description: Creates a duplicate of this section.
type: docs
weight: 79
url: /cpp/aspose.words/section/clone/
---
## Section::Clone method


Creates a duplicate of this section.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


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

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
