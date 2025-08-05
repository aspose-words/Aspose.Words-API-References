---
title: Aspose::Words::DocumentBuilder::MoveToSection method
linktitle: MoveToSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::MoveToSection method. Moves the cursor to the beginning of the body in a specified section in C++.'
type: docs
weight: 60000
url: /cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Moves the cursor to the beginning of the body in a specified section.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| sectionIndex | int32_t | The index of the section to move to. |
## Remarks


When *sectionIndex* is greater than or equal to 0, it specifies an index from the beginning of the document with 0 being the first section. When *sectionIndex* is less than 0, it specified an index from the end of the document with -1 being the last section.

The cursor is moved to the first paragraph in the [Body](../../body/) of the specified section.

## Examples



Shows how to create headers and footers in a document using [DocumentBuilder](../). 
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

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
