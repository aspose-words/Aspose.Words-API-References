---
title: get_SheetsPerBooklet
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the number of pages to be included in each booklet.
type: docs
weight: 508
url: /cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Returns or sets the number of pages to be included in each booklet.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


## Examples



Shows how to configure a document that can be printed as a book fold. 
```cpp
auto doc = MakeObject<Document>();

// Insert text that spans 16 pages.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder->InsertBreak(BreakType::PageBreak);
    builder->Write(String::Format(u"Booklet face #{0}", i));
}

// Configure the first section's "PageSetup" property to print the document in the form of a book fold.
// When we print this document on both sides, we can take the pages to stack them
// and fold them all down the middle at once. The contents of the document will line up into a book fold.
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(MultiplePagesType::BookFoldPrinting);

// We can only specify the number of sheets in multiples of 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(ArtifactsDir + u"PageSetup.Booklet.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
