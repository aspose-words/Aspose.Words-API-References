---
title: get_ImageSavingCallback
second_title: Aspose.Words for C++ API Reference
description: Allows to control how images are saved when a document is saved to Markdown format.
type: docs
weight: 27
url: /cpp/aspose.words.saving/markdownsaveoptions/get_imagesavingcallback/
---
## MarkdownSaveOptions.get_ImageSavingCallback method


Allows to control how images are saved when a document is saved to **Markdown** format.

```cpp
System::SharedPtr<Aspose::Words::Saving::IImageSavingCallback> Aspose::Words::Saving::MarkdownSaveOptions::get_ImageSavingCallback() const
```


## Examples




Shows how to rename the image name during saving into Markdown document. 
```cpp
void RenameImages()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

    auto options = MakeObject<MarkdownSaveOptions>();

    // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
    // Each image will be in the form of a file in the local file system.
    // There is also a callback that can customize the name and file system location of each image.
    options->set_ImageSavingCallback(MakeObject<ExDocumentBuilder::SavedImageRename>(u"DocumentBuilder.HandleDocument.md"));

    // The ImageSaving() method of our callback will be run at this time.
    doc->Save(ArtifactsDir + u"DocumentBuilder.HandleDocument.md", options);

    ASSERT_EQ(1, System::IO::Directory::GetFiles(ArtifactsDir)
                     ->LINQ_Where([](String s) { return s.StartsWith(ArtifactsDir + u"DocumentBuilder.HandleDocument.md shape"); })
                     ->LINQ_Count([](String f) { return f.EndsWith(u".jpeg"); }));
    ASSERT_EQ(8, System::IO::Directory::GetFiles(ArtifactsDir)
                     ->LINQ_Where([](String s) { return s.StartsWith(ArtifactsDir + u"DocumentBuilder.HandleDocument.md shape"); })
                     ->LINQ_Count([](String f) { return f.EndsWith(u".png"); }));
}

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

        args->set_ImageFileName(imageFileName);
        args->set_ImageStream(MakeObject<System::IO::FileStream>(ArtifactsDir + imageFileName, System::IO::FileMode::Create));

        ASSERT_TRUE(args->get_ImageStream()->get_CanWrite());
        ASSERT_TRUE(args->get_IsImageAvailable());
        ASSERT_FALSE(args->get_KeepImageStreamOpen());
    }
};
```

