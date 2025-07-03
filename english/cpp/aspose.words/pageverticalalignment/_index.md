---
title: Aspose::Words::PageVerticalAlignment enum
linktitle: PageVerticalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageVerticalAlignment enum. Specifies vertical justification of text on each page in C++.'
type: docs
weight: 108000
url: /cpp/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enum


Specifies vertical justification of text on each page.

```cpp
enum class PageVerticalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Bottom | 3 | Text is aligned at the bottom of the page. |
| Center | 1 | Text is aligned in the middle of the page. |
| Justify | 2 | Text is spread to fill the page. |
| Top | 0 | Text is aligned at the top of the page. |


## Examples



Shows how to apply and revert page setup settings to sections in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modify the page setup properties for the builder's current section and add text.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// If we start a new section using a document builder,
// it will inherit the builder's current page setup properties.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
