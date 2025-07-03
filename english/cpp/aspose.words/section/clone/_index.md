---
title: Aspose::Words::Section::Clone method
linktitle: Clone
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Section::Clone method. Creates a duplicate of this section in C++.'
type: docs
weight: 7000
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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Delete the first section from the document.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Append a copy of what is now the first section to the end of the document.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## See Also

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
