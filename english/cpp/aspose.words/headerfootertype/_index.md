---
title: Aspose::Words::HeaderFooterType enum
linktitle: HeaderFooterType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HeaderFooterType enum. Identifies the type of header or footer found in a Word file in C++.'
type: docs
weight: 90000
url: /cpp/aspose.words/headerfootertype/
---
## HeaderFooterType enum


Identifies the type of header or footer found in a Word file.

```cpp
enum class HeaderFooterType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| HeaderEven | 0 | Header for even numbered pages. |
| HeaderPrimary | 1 | Primary header, also used for odd numbered pages. |
| FooterEven | 2 | Footer for even numbered pages. |
| FooterPrimary | 3 | Primary footer, also used for odd numbered pages. |
| HeaderFirst | 4 | Header for the first page of the section. |
| FooterFirst | 5 | Footer for the first page of the section. |


## Examples



Shows how to create headers and footers in a document using [DocumentBuilder](../documentbuilder/). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(true);
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(true);

// Create the headers, then add three pages to the document to display each header type.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Write(u"Header for the first page");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Write(u"Header for even pages");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Header for all other pages");

builder->MoveToSection(0);
builder->Writeln(u"Page1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page3");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.HeadersAndFooters.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
