---
title: HeaderFooterType
second_title: Aspose.Words for C++ API Reference
description: Identifies the type of header or footer found in a Word file.
type: docs
weight: 1158
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(true);
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(true);

// Create the headers, then add three pages to the document to display each header type.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderFirst);
builder->Write(u"Header for the first page");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderEven);
builder->Write(u"Header for even pages");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Write(u"Header for all other pages");

builder->MoveToSection(0);
builder->Writeln(u"Page1");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page2");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page3");

doc->Save(ArtifactsDir + u"DocumentBuilder.HeadersAndFooters.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
