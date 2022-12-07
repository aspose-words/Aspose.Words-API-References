---
title: get_IsImageAvailable
second_title: Aspose.Words for C++ API Reference
description: Returns true if the current image is available for export.
type: docs
weight: 66
url: /cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Returns **true** if the current image is available for export.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Remarks


Some images in the document can be unavailable, for example, because the image is linked and the link is inaccessible or does not point to a valid image. In this case Aspose.Words exports an icon with a red cross. This property returns **true** if the original image is available; returns **false** if the original image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property is always **true**.

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
