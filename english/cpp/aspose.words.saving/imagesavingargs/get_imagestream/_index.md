---
title: get_ImageStream
second_title: Aspose.Words for C++ API Reference
description: Allows to specify the stream where the image will be saved to.
type: docs
weight: 40
url: /cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs.get_ImageStream method


Allows to specify the stream where the image will be saved to.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```


This property allows you to save images to streams instead of files during HTML.

The default value is **null**. When this property is **null**, the image will be saved to a file specified in the [ImageFileName](../get_imagefilename/) property.

Using [IImageSavingCallback](../../iimagesavingcallback/) you cannot substitute one image with another. It is intended only for control over location where to save images.

## Examples




Shows how to involve an image saving callback in an HTML conversion process. 
```cpp
void ImageSavingCallback()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

    // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
    // to customize the image saving process.
    auto options = MakeObject<HtmlSaveOptions>();
    options->set_ImageSavingCallback(MakeObject<ExHtmlSaveOptions::ImageShapePrinter>());

    doc->Save(ArtifactsDir + u"HtmlSaveOptions.ImageSavingCallback.html", options);
}

class ImageShapePrinter : public IImageSavingCallback
{
public:
    ImageShapePrinter() : mImageCount(0)
    {
    }

private:
    int mImageCount;

    void ImageSaving(SharedPtr<ImageSavingArgs> args) override
    {
        args->set_KeepImageStreamOpen(false);
        ASSERT_TRUE(args->get_IsImageAvailable());

        std::cout << args->get_Document()->get_OriginalFileName().Split(MakeArray<char16_t>({u'\\'}))->LINQ_Last() << " Image #" << ++mImageCount
                  << std::endl;

        auto layoutCollector = MakeObject<LayoutCollector>(args->get_Document());

        std::cout << "\tOn page:\t" << layoutCollector->GetStartPageIndex(args->get_CurrentShape()) << std::endl;
        std::cout << "\tDimensions:\t" << args->get_CurrentShape()->get_Bounds() << std::endl;
        std::cout << String::Format(u"\tAlignment:\t{0}", args->get_CurrentShape()->get_VerticalAlignment()) << std::endl;
        std::cout << String::Format(u"\tWrap type:\t{0}", args->get_CurrentShape()->get_WrapType()) << std::endl;
        std::cout << "Output filename:\t" << args->get_ImageFileName() << "\n" << std::endl;
    }
};
```

