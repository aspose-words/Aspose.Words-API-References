---
title: Aspose::Words::PageSetup::get_PageStartingNumber method
linktitle: get_PageStartingNumber
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_PageStartingNumber method. Gets or sets the starting page number of the section in C++.'
type: docs
weight: 35000
url: /cpp/aspose.words/pagesetup/get_pagestartingnumber/
---
## PageSetup::get_PageStartingNumber method


Gets or sets the starting page number of the section.

```cpp
int32_t Aspose::Words::PageSetup::get_PageStartingNumber()
```


## Examples



Shows how to set up page numbering in a section. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Move the document builder to the first section's primary header,
// which every page in that section will display.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Insert a PAGE field, which will display the number of the current page.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configure the section to have the page count that PAGE fields display start from 5.
// Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Create another primary header for the second section, with another PAGE field.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configure the section to have the page count that PAGE fields display start from 10.
// Also, configure all PAGE fields to display their page numbers using Arabic numbers.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
