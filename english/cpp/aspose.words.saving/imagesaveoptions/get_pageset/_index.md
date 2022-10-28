---
title: get_PageSet
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the pages to render. Default is all the pages in the document.
type: docs
weight: 105
url: /cpp/aspose.words.saving/imagesaveoptions/get_pageset/
---
## ImageSaveOptions.get_PageSet method


Gets or sets the pages to render. Default is all the pages in the document.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::ImageSaveOptions::get_PageSet()
```


This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.

## Examples




Shows how to render one page from a document to a JPEG image. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(ImageDir + u"Logo.jpg");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = MakeObject<ImageSaveOptions>(SaveFormat::Jpeg);

// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options->set_PageSet(MakeObject<PageSet>(1));

// When we save the document to the JPEG format, Aspose.Words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc->Save(ArtifactsDir + u"ImageSaveOptions.OnePage.jpg", options);
```


Shows how to specify which page in a document to render as an image. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world! This is page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"This is page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"This is page 3.");

ASSERT_EQ(3, doc->get_PageCount());

// When we save the document as an image, Aspose.Words only renders the first page by default.
// We can pass a SaveOptions object to specify a different page to render.
auto saveOptions = MakeObject<ImageSaveOptions>(SaveFormat::Gif);

// Render every page of the document to a separate image file.
for (int i = 1; i <= doc->get_PageCount(); i++)
{
    saveOptions->set_PageSet(MakeObject<PageSet>(1));

    doc->Save(ArtifactsDir + String::Format(u"ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
}
```


Shows how to render every page of a document to a separate TIFF image. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(ImageDir + u"Logo.jpg");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = MakeObject<ImageSaveOptions>(SaveFormat::Tiff);

for (int i = 0; i < doc->get_PageCount(); i++)
{
    // Set the "PageSet" property to the number of the first page from
    // which to start rendering the document from.
    options->set_PageSet(MakeObject<PageSet>(i));

    doc->Save(ArtifactsDir + String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Shows how to extract pages based on exact page ranges. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

auto imageOptions = MakeObject<ImageSaveOptions>(SaveFormat::Tiff);
auto pageSet = MakeObject<PageSet>(MakeArray<SharedPtr<PageRange>>(
    {MakeObject<PageRange>(1, 1), MakeObject<PageRange>(2, 3), MakeObject<PageRange>(1, 3), MakeObject<PageRange>(2, 4), MakeObject<PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(ArtifactsDir + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

