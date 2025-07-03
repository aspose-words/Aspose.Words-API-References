---
title: Aspose::Words::Orientation enum
linktitle: Orientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Orientation enum. Specifies page orientation in C++.'
type: docs
weight: 104000
url: /cpp/aspose.words/orientation/
---
## Orientation enum


Specifies page orientation.

```cpp
enum class Orientation
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Portrait | 1 | Portrait page orientation (narrow and tall). |
| Landscape | 2 | Landscape page orientation (wide and short). |


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
