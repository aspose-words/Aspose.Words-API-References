---
title: Aspose::Words::Drawing::ImageType enum
linktitle: ImageType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageType enum. Specifies the type (format) of an image in a Microsoft Word document in C++.'
type: docs
weight: 28000
url: /cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Specifies the type (format) of an image in a Microsoft Word document.

```cpp
enum class ImageType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| NoImage | 0 | The is no image data. |
| Unknown | 1 | An unknown image type or image type that cannot be directly stored inside a Microsoft Word document. |
| Emf | 2 | Windows Enhanced Metafile. |
| Wmf | 3 | Windows Metafile. |
| Pict | 4 | Macintosh PICT. An existing image will be preserved in a document, but inserting new PICT images into a document is not supported. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Portable Network Graphics. |
| Bmp | 7 | Windows Bitmap. |
| Eps | 8 | Encapsulated PostScript. |
| WebP | 9 |  |


## Examples



Shows how to add an image to a shape and check its type. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

ArrayPtr<uint8_t> imageBytes = System::IO::File::ReadAllBytes(ImageDir + u"Logo.jpg");

{
    auto stream = MakeObject<System::IO::MemoryStream>(imageBytes);
    SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);

    // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
    SharedPtr<Shape> imgShape = builder->InsertImage(image);
    ASSERT_EQ(ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
}
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
