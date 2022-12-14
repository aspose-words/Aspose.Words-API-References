---
title: get_PageNumberStyle
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the page number format.
type: docs
weight: 430
url: /cpp/aspose.words/pagesetup/get_pagenumberstyle/
---
## PageSetup::get_PageNumberStyle method


Gets or sets the page number format.

```cpp
Aspose::Words::NumberStyle Aspose::Words::PageSetup::get_PageNumberStyle()
```


## Examples



Shows how to set up page numbering in a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Move the document builder to the first section's primary header,
// which every page in that section will display.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);

// Insert a PAGE field, which will display the number of the current page.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configure the section to have the page count that PAGE fields display start from 5.
// Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(NumberStyle::UppercaseRoman);

// Create another primary header for the second section, with another PAGE field.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configure the section to have the page count that PAGE fields display start from 10.
// Also, configure all PAGE fields to display their page numbers using Arabic numbers.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(NumberStyle::Arabic);

doc->Save(ArtifactsDir + u"PageSetup.PageNumbering.docx");
```

## See Also

* Enum [NumberStyle](../../numberstyle/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
