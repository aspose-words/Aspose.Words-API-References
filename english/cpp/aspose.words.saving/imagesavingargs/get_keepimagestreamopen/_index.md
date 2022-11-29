---
title: get_KeepImageStreamOpen
second_title: Aspose.Words for C++ API Reference
description: Specifies whether Aspose.Words should keep the stream open or close it after saving an image.
type: docs
weight: 66
url: /cpp/aspose.words.saving/imagesavingargs/get_keepimagestreamopen/
---
## ImageSavingArgs::get_KeepImageStreamOpen method


Specifies whether Aspose.Words should keep the stream open or close it after saving an image.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen() const
```

## Remarks


Default is **false** and Aspose.Words will close the stream you provided in the [ImageStream](../get_imagestream/) property after writing an image into it. Specify **true** to keep the stream open.

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

## See Also

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
