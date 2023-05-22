---
title: Aspose::Words::Document::Save method
linktitle: Save
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::Save method. Saves the document to a stream using the specified format in C++.'
type: docs
weight: 72000
url: /cpp/aspose.words/document/save/
---
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Saves the document to a stream using the specified format.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Stream where to save the document. |
| saveFormat | Aspose::Words::SaveFormat | The format in which to save the document. |

### ReturnValue

Additional information that you can optionally use.

## Examples



Shows how to save a document to an image via stream, and then read the image from that stream. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(ImageDir + u"Logo.jpg");

{
    auto stream = MakeObject<System::IO::MemoryStream>();
    doc->Save(stream, SaveFormat::Bmp);

    stream->set_Position(0);

    // Read the stream back into an image.
    {
        SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        ASPOSE_ASSERT_EQ(System::Drawing::Imaging::ImageFormat::get_Bmp(), image->get_RawFormat());
        ASSERT_EQ(816, image->get_Width());
        ASSERT_EQ(1056, image->get_Height());
    }
}
```


Shows how to save a document to a stream. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

{
    auto dstStream = MakeObject<System::IO::MemoryStream>();
    doc->Save(dstStream, SaveFormat::Docx);

    // Verify that the stream contains the document.
    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", MakeObject<Document>(dstStream)->GetText().Trim());
}
```

## See Also

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Saves the document to a stream using the specified save options.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Stream where to save the document. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Specifies the options that control how the document is saved. Can be **null**. If this is **null**, the document will be saved in the binary DOC format. |

### ReturnValue

Additional information that you can optionally use.

## Examples



Shows how to convert only some of the pages in a document to PDF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 3.");

{
    SharedPtr<System::IO::Stream> stream = System::IO::File::Create(ArtifactsDir + u"PdfSaveOptions.OnePage.pdf");
    // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
    // to modify how that method converts the document to .PDF.
    auto options = MakeObject<PdfSaveOptions>();

    // Set the "PageIndex" to "1" to render a portion of the document starting from the second page.
    options->set_PageSet(MakeObject<PageSet>(1));

    // This document will contain one page starting from page two, which will only contain the second page.
    doc->Save(stream, options);
}
```

## See Also

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&) method


Saves the document to a file. Automatically determines the save format from the extension.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

### ReturnValue

Additional information that you can optionally use.

## Examples



Shows how to open a document and convert it to .PDF. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

doc->Save(ArtifactsDir + u"Document.ConvertToPdf.pdf");
```

## See Also

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, Aspose::Words::SaveFormat) method


Saves the document to a file in the specified format.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveFormat | Aspose::Words::SaveFormat | The format in which to save the document. |

### ReturnValue

Additional information that you can optionally use.

## Examples



Shows how to convert from DOCX to HTML format. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

doc->Save(ArtifactsDir + u"Document.ConvertToHtml.html", SaveFormat::Html);
```

## See Also

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Saves the document to a file using the specified save options.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Specifies the options that control how the document is saved. Can be **null**. |

### ReturnValue

Additional information that you can optionally use.

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


Shows how to configure compression while saving a document as a JPEG. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertImage(ImageDir + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto imageOptions = MakeObject<ImageSaveOptions>(SaveFormat::Jpeg);

// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions->set_JpegQuality(10);

doc->Save(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

ASSERT_GE(20000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighCompression.jpg")->get_Length());

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions->set_JpegQuality(100);

doc->Save(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

ASSERT_LT(60000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"ImageSaveOptions.JpegQuality.HighQuality.jpg")->get_Length());
```


Shows how to convert a whole document to PDF with three levels in the document outline. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert headings of levels 1 to 5.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading4);

builder->Writeln(u"Heading 1.2.2.1");
builder->Writeln(u"Heading 1.2.2.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading5);

builder->Writeln(u"Heading 1.2.2.2.1");
builder->Writeln(u"Heading 1.2.2.2.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options->get_OutlineOptions()->set_HeadingsOutlineLevels(4);

// If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
// an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
// In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
// the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
// In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
// Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
// and collapse all level and 3 and higher entries when we open the document.
options->get_OutlineOptions()->set_ExpandedOutlineLevels(2);

doc->Save(ArtifactsDir + u"PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

## See Also

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, Aspose::Words::SaveFormat saveFormat)
```

## See Also

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)
```

## See Also

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
