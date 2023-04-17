---
title: Aspose::Words::DocumentBuilder::MoveToHeaderFooter method
linktitle: MoveToHeaderFooter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::MoveToHeaderFooter method. Moves the cursor to the beginning of a header or footer in the current section in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


Moves the cursor to the beginning of a header or footer in the current section.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Specifies the header or footer to move to. |
## Remarks


After you moved the cursor into a header or footer, you can use the rest of [DocumentBuilder](../) methods to modify the contents of the header or footer.

If you want to create headers and footers different for the first page, you need to set [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/).

If you want to create headers and footers different for even and odd pages, you need to set [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/).

Use [MoveToSection()](../movetosection/) to move out of the header into the main text.

## Examples



Shows how to create headers and footers in a document using [DocumentBuilder](../). 
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


Shows how to insert an image, and use it as a watermark. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert the image into the header so that it will be visible on every page.
SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Transparent background logo.png");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
SharedPtr<Shape> shape = builder->InsertImage(image);
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);

// Place the image at the center of the page.
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertWatermark.docx");
```

## See Also

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
