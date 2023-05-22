---
title: Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape method
linktitle: get_CurrentShape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape method. Gets the ShapeBase object corresponding to the shape or group shape that is about to be saved in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Gets the [ShapeBase](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape that is about to be saved.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Remarks


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document. You can use the [CurrentShape](./) property to generate a "better" file name by examining shape properties such as [Title](../../../aspose.words.drawing/imagedata/get_title/) (Shape only), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (Shape only) and [Name](../../../aspose.words.drawing/shapebase/get_name/). Of course you can build file names using any other properties or criteria but note that subsidiary file names must be unique within the export operation.

Some images in the document can be unavailable. To check image availability use the [IsImageAvailable](../get_isimageavailable/) property.

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

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
