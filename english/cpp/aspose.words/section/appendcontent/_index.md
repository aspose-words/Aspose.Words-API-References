---
title: AppendContent
second_title: Aspose.Words for C++ API Reference
description: Inserts a copy of content of the source section at the end of this section.
type: docs
weight: 40
url: /cpp/aspose.words/section/appendcontent/
---
## Section::AppendContent method


Inserts a copy of content of the source section at the end of this section.

```cpp
void Aspose::Words::Section::AppendContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Parameter | Type | Description |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | The section to copy content from. |
## Remarks


Only content of [Body](../get_body/) of the source section is copied, page setup, headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.

## Examples



Shows how to append the contents of a section to another section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

SharedPtr<Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(String(u"Section 3") + ControlChar::SectionBreak(), section->GetText());

// Insert the contents of the first section to the beginning of the third section.
SharedPtr<Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// Insert the contents of the second section to the end of the third section.
SharedPtr<Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// The "PrependContent" and "AppendContent" methods did not create any new sections.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(String(u"Section 1") + ControlChar::ParagraphBreak() + u"Section 3" + ControlChar::ParagraphBreak() + u"Section 2" +
              ControlChar::SectionBreak(),
          section->GetText());
```

## See Also

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
