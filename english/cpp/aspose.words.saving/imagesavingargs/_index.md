---
title: ImageSavingArgs
second_title: Aspose.Words for C++ API Reference
description: Provides data for the ImageSaving() event. To learn more, visit the  documentation article.
type: docs
weight: 144
url: /cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Provides data for the [ImageSaving()](../iimagesavingcallback/imagesaving/) event. To learn more, visit the [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) documentation article.

```cpp
class ImageSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Gets the [ShapeBase](../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape that is about to be saved. |
| [get_Document](./get_document/)() | Gets the document object that is currently being saved. |
| [get_ImageFileName](./get_imagefilename/)() const | Gets or sets the file name (without path) where the image will be saved to. |
| [get_ImageStream](./get_imagestream/)() const | Allows to specify the stream where the image will be saved to. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Returns **true** if the current image is available for export. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Setter for [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Setter for [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Remarks


By default, when Aspose.Words saves a document to HTML, it saves each image into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) and [IsImageAvailable](./get_isimageavailable/) properties.

To save images into streams instead of files, use the [ImageStream](./get_imagestream/) property.

## Examples



Shows how to split a document into parts and save them. 
```cpp
void DocumentPartsFileNames()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");
    String outFileName = u"SavingCallback.DocumentPartsFileNames.html";

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    auto options = MakeObject<HtmlSaveOptions>();

    // If we save the document normally, there will be one output HTML
    // document with all the source document's contents.
    // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
    // save our document to multiple HTML files: one for each section.
    options->set_DocumentSplitCriteria(DocumentSplitCriteria::SectionBreak);

    // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
    options->set_DocumentPartSavingCallback(MakeObject<ExSavingCallback::SavedDocumentPartRename>(outFileName, options->get_DocumentSplitCriteria()));

    // If we convert a document that contains images into html, we will end up with one html file which links to several images.
    // Each image will be in the form of a file in the local file system.
    // There is also a callback that can customize the name and file system location of each image.
    options->set_ImageSavingCallback(MakeObject<ExSavingCallback::SavedImageRename>(outFileName));

    doc->Save(ArtifactsDir + outFileName, options);
}

class SavedDocumentPartRename : public IDocumentPartSavingCallback
{
public:
    SavedDocumentPartRename(String outFileName, DocumentSplitCriteria documentSplitCriteria)
        : mCount(0), mDocumentSplitCriteria(((Aspose::Words::Saving::DocumentSplitCriteria)0))
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

private:
    int mCount;
    String mOutFileName;
    DocumentSplitCriteria mDocumentSplitCriteria;

    void DocumentPartSaving(SharedPtr<DocumentPartSavingArgs> args) override
    {
        // We can access the entire source document via the "Document" property.
        ASSERT_TRUE(args->get_Document()->get_OriginalFileName().EndsWith(u"Rendering.docx"));

        String partType = String::Empty;

        switch (mDocumentSplitCriteria)
        {
        case DocumentSplitCriteria::PageBreak:
            partType = u"Page";
            break;

        case DocumentSplitCriteria::ColumnBreak:
            partType = u"Column";
            break;

        case DocumentSplitCriteria::SectionBreak:
            partType = u"Section";
            break;

        case DocumentSplitCriteria::HeadingParagraph:
            partType = u"Paragraph from heading";
            break;

        default:
            break;
        }

        String partFileName = String::Format(u"{0} part {1}, of type {2}{3}", mOutFileName, ++mCount, partType,
                                             System::IO::Path::GetExtension(args->get_DocumentPartFileName()));

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output part file:
        args->set_DocumentPartFileName(partFileName);

        // 2 -  Create a custom stream for the output part file:
        args->set_DocumentPartStream(MakeObject<System::IO::FileStream>(ArtifactsDir + partFileName, System::IO::FileMode::Create));

        ASSERT_TRUE(args->get_DocumentPartStream()->get_CanWrite());
        ASSERT_FALSE(args->get_KeepDocumentPartStreamOpen());
    }
};

class SavedImageRename : public IImageSavingCallback
{
public:
    SavedImageRename(String outFileName) : mCount(0)
    {
        mOutFileName = outFileName;
    }

private:
    int mCount;
    String mOutFileName;

    void ImageSaving(SharedPtr<ImageSavingArgs> args) override
    {
        String imageFileName = String::Format(u"{0} shape {1}, of type {2}{3}", mOutFileName, ++mCount, args->get_CurrentShape()->get_ShapeType(),
                                              System::IO::Path::GetExtension(args->get_ImageFileName()));

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output image file:
        args->set_ImageFileName(imageFileName);

        // 2 -  Create a custom stream for the output image file:
        args->set_ImageStream(MakeObject<System::IO::FileStream>(ArtifactsDir + imageFileName, System::IO::FileMode::Create));

        ASSERT_TRUE(args->get_ImageStream()->get_CanWrite());
        ASSERT_TRUE(args->get_IsImageAvailable());
        ASSERT_FALSE(args->get_KeepImageStreamOpen());
    }
};
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
