---
title: get_ScaleImageToShapeSize
second_title: Aspose.Words for C++ API Reference
description: Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is true.
type: docs
weight: 573
url: /cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Remarks


An image in a Microsoft Word document is a shape. The shape has a size and the image has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size. The [ScaleImageToShapeSize](./) property controls where the scaling of the image takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [ScaleImageToShapeSize](./) is **true**, the image is scaled by [Aspose.Words](../../../aspose.words/) using high quality scaling during export to HTML. When [ScaleImageToShapeSize](./) is **false**, the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better display quality in the browser and smaller file size when [ScaleImageToShapeSize](./) is **true**, but better printing quality and faster conversion when [ScaleImageToShapeSize](./) is **false**.

## Examples



Shows how to disable the scaling of images to their parent shape dimensions when saving to .html. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a shape which contains an image, and then make that shape considerably smaller than the image.
SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Transparent background logo.png");

ASSERT_EQ(400, image->get_Size().get_Width());
ASSERT_EQ(400, image->get_Size().get_Height());

SharedPtr<Shape> imageShape = builder->InsertImage(image);
imageShape->set_Width(50);
imageShape->set_Height(50);

// Saving a document that contains shapes with images to HTML will create an image file in the local file system
// for each such shape. The output HTML document will use <image> tags to link to and display these images.
// When we save the document to HTML, we can pass a SaveOptions object to determine
// whether to scale all images that are inside shapes to the sizes of their shapes.
// Setting the "ScaleImageToShapeSize" flag to "true" will shrink every image
// to the size of the shape that contains it, so that no saved images will be larger than the document requires them to be.
// Setting the "ScaleImageToShapeSize" flag to "false" will preserve these images' original sizes,
// which will take up more space in exchange for preserving image quality.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ScaleImageToShapeSize(scaleImageToShapeSize);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ScaleImageToShapeSize.html", options);

auto fileInfo = MakeObject<System::IO::FileInfo>(ArtifactsDir + u"HtmlSaveOptions.ScaleImageToShapeSize.001.png");
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
