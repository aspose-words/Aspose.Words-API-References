---
title: Aspose::Words::DocumentBuilder::set_Document method
linktitle: set_Document
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::set_Document method. Sets the Document object that this object is attached to in C++.'
type: docs
weight: 93000
url: /cpp/aspose.words/documentbuilder/set_document/
---
## DocumentBuilder::set_Document method


Sets the [Document](../get_document/) object that this object is attached to.

```cpp
void Aspose::Words::DocumentBuilder::set_Document(const System::SharedPtr<Aspose::Words::Document> & value)
```

## Examples


Shows how to apply and revert page setup settings to sections in a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modify the page setup properties for the builder's current section and add text.
builder->get_PageSetup()->set_Orientation(Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// If we start a new section using a document builder,
// it will inherit the builder's current page setup properties.
builder->InsertBreak(BreakType::SectionBreakNewPage);

ASSERT_EQ(Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```
## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
