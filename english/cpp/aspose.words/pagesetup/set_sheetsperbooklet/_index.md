---
title: Aspose::Words::PageSetup::set_SheetsPerBooklet method
linktitle: set_SheetsPerBooklet
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::set_SheetsPerBooklet method. Sets the number of pages to be included in each booklet in C++.'
type: docs
weight: 86000
url: /cpp/aspose.words/pagesetup/set_sheetsperbooklet/
---
## PageSetup::set_SheetsPerBooklet method


Sets the number of pages to be included in each booklet.

```cpp
void Aspose::Words::PageSetup::set_SheetsPerBooklet(int32_t value)
```

## Examples


Shows how to configure a document that can be printed as a book fold.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insert text that spans 16 pages.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Configure the first section's "PageSetup" property to print the document in the form of a book fold.
// When we print this document on both sides, we can take the pages to stack them
// and fold them all down the middle at once. The contents of the document will line up into a book fold.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(MultiplePagesType::BookFoldPrinting);

// We can only specify the number of sheets in multiples of 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```
## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
