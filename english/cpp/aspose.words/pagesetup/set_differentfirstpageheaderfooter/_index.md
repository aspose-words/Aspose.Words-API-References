---
title: Aspose::Words::PageSetup::set_DifferentFirstPageHeaderFooter method
linktitle: set_DifferentFirstPageHeaderFooter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::set_DifferentFirstPageHeaderFooter method. True if a different header or footer is used on the first page in C++.'
type: docs
weight: 59000
url: /cpp/aspose.words/pagesetup/set_differentfirstpageheaderfooter/
---
## PageSetup::set_DifferentFirstPageHeaderFooter method


True if a different header or footer is used on the first page.

```cpp
void Aspose::Words::PageSetup::set_DifferentFirstPageHeaderFooter(bool value)
```

## Examples


Shows how to enable or disable primary headers/footers.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are two types of header/footers.
// 1 -  The "First" header/footer, which appears on the first page of the section.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  The "Primary" header/footer, which appears on every page in the section.
// We can override the primary header/footer by a first and an even page header/footer.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Each section has a "PageSetup" object that specifies page appearance-related properties
// such as orientation, size, and borders.
// Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
// Set the "DifferentFirstPageHeaderFooter" property to "false"
// to make the first page display the primary header/footer.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```
## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
