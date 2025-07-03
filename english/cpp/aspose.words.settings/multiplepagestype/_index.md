---
title: Aspose::Words::Settings::MultiplePagesType enum
linktitle: MultiplePagesType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::MultiplePagesType enum. Specifies how document is printed out in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


Specifies how document is printed out.

```cpp
enum class MultiplePagesType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | 0 | Normal printing, no multiple pages specified. |
| MirrorMargins | 1 | Swaps left and right margins on facing pages. |
| TwoPagesPerSheet | 2 | Prints two pages per sheet. |
| BookFoldPrinting | 3 | Specifies whether to print the document as a book fold. |
| BookFoldPrintingReverse | 4 | Specifies whether to print the document as a reverse book fold. |
| Default | n/a | Default value is [Normal](./) |


## Examples



Shows how to configure a document that can be printed as a book fold. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insert text that spans 16 pages.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Configure the first section's "PageSetup" property to print the document in the form of a book fold.
// When we print this document on both sides, we can take the pages to stack them
// and fold them all down the middle at once. The contents of the document will line up into a book fold.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// We can only specify the number of sheets in multiples of 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
