---
title: InsertImage
second_title: Aspose.Words for C++ API Reference
description: Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.
type: docs
weight: 469
url: /cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | The byte array that contains the image. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from a byte array into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");

{
    auto ms = MakeObject<System::IO::MemoryStream>();
    image->Save(ms, System::Drawing::Imaging::ImageFormat::get_Png());
    ArrayPtr<uint8_t> imageByteArray = ms->ToArray();

    // Below are three ways of inserting an image from a byte array.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder->InsertImage(imageByteArray);

    builder->InsertBreak(BreakType::PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder->InsertImage(imageByteArray, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(BreakType::PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder->InsertImage(imageByteArray, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0,
                         WrapType::Square);
}

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts an image from a byte array at the specified position and size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | The byte array that contains the image. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | double | Distance in points from the origin to the left side of the image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | double | Distance in points from the origin to the top side of the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the image. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from a byte array into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");

{
    auto ms = MakeObject<System::IO::MemoryStream>();
    image->Save(ms, System::Drawing::Imaging::ImageFormat::get_Png());
    ArrayPtr<uint8_t> imageByteArray = ms->ToArray();

    // Below are three ways of inserting an image from a byte array.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder->InsertImage(imageByteArray);

    builder->InsertBreak(BreakType::PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder->InsertImage(imageByteArray, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(BreakType::PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder->InsertImage(imageByteArray, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0,
                         WrapType::Square);
}

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Inserts an inline image from a byte array into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | The byte array that contains the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from a byte array into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");

{
    auto ms = MakeObject<System::IO::MemoryStream>();
    image->Save(ms, System::Drawing::Imaging::ImageFormat::get_Png());
    ArrayPtr<uint8_t> imageByteArray = ms->ToArray();

    // Below are three ways of inserting an image from a byte array.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder->InsertImage(imageByteArray);

    builder->InsertBreak(BreakType::PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder->InsertImage(imageByteArray, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(BreakType::PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder->InsertImage(imageByteArray, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0,
                         WrapType::Square);
}

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Inserts an image from a **Image** object into the document. The image is inserted inline and at 100% scale.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | The image to insert into the document. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from an object into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");

// Below are three ways of inserting an image from an Image object instance.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder->InsertImage(image);

builder->InsertBreak(BreakType::PageBreak);

// 2 -  Inline shape with custom dimensions:
builder->InsertImage(image, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

builder->InsertBreak(BreakType::PageBreak);

// 3 -  Floating shape with custom dimensions:
builder->InsertImage(image, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts an image from a **Image** object at the specified position and size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | The image to insert into the document. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | double | Distance in points from the origin to the left side of the image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | double | Distance in points from the origin to the top side of the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the image. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from an object into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");

// Below are three ways of inserting an image from an Image object instance.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder->InsertImage(image);

builder->InsertBreak(BreakType::PageBreak);

// 2 -  Inline shape with custom dimensions:
builder->InsertImage(image, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

builder->InsertBreak(BreakType::PageBreak);

// 3 -  Floating shape with custom dimensions:
builder->InsertImage(image, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


Inserts an inline image from a **Image** object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | The image to insert into the document. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from an object into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");

// Below are three ways of inserting an image from an Image object instance.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder->InsertImage(image);

builder->InsertBreak(BreakType::PageBreak);

// 2 -  Inline shape with custom dimensions:
builder->InsertImage(image, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

builder->InsertBreak(BreakType::PageBreak);

// 3 -  Floating shape with custom dimensions:
builder->InsertImage(image, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Inserts an image from a stream into the document. The image is inserted inline and at 100% scale.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream that contains the image. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from a stream into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

{
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(ImageDir + u"Logo.jpg");
    // Below are three ways of inserting an image from a stream.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder->InsertImage(stream);

    builder->InsertBreak(BreakType::PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder->InsertImage(stream, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(BreakType::PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder->InsertImage(stream, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, WrapType::Square);
}

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Shows how to insert a shape with an image from a stream into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

{
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(ImageDir + u"Logo.jpg");
    builder->Write(u"Image from stream: ");
    builder->InsertImage(stream);
}

doc->Save(ArtifactsDir + u"Image.FromStream.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts an image from a stream at the specified position and size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream that contains the image. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | double | Distance in points from the origin to the left side of the image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | double | Distance in points from the origin to the top side of the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the image. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from a stream into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

{
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(ImageDir + u"Logo.jpg");
    // Below are three ways of inserting an image from a stream.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder->InsertImage(stream);

    builder->InsertBreak(BreakType::PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder->InsertImage(stream, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(BreakType::PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder->InsertImage(stream, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, WrapType::Square);
}

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Inserts an inline image from a stream into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream that contains the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from a stream into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

{
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(ImageDir + u"Logo.jpg");
    // Below are three ways of inserting an image from a stream.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder->InsertImage(stream);

    builder->InsertBreak(BreakType::PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder->InsertImage(stream, ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(BreakType::PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder->InsertImage(stream, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, WrapType::Square);
}

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The file with the image. Can be any valid local or remote URI. |

### ReturnValue

The image node that was just inserted.
## Remarks


This overload will automatically download the image before inserting into the document if you specify a remote URI.

You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from the local file system into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are three ways of inserting an image from a local system filename.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder->InsertImage(ImageDir + u"Logo.jpg");

builder->InsertBreak(BreakType::PageBreak);

// 2 -  Inline shape with custom dimensions:
builder->InsertImage(ImageDir + u"Transparent background logo.png", ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

builder->InsertBreak(BreakType::PageBreak);

// 3 -  Floating shape with custom dimensions:
builder->InsertImage(ImageDir + u"Windows MetaFile.wmf", RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0,
                     100.0, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Shows how to determine which image will be inserted. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->InsertImage(ImageDir + u"Scalable Vector Graphics.svg");

// Aspose.Words insert SVG image to the document as PNG with svgBlip extension
// that contains the original vector SVG image representation.
doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(MsWordVersion::Word2003);

// Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Shows how to insert gif image to the document. 
```cpp
auto builder = MakeObject<DocumentBuilder>();

// We can insert gif image using path or bytes array.
// It works only if DocumentBuilder optimized to Word version 2010 or higher.
// Note, that access to the image bytes causes conversion Gif to Png.
SharedPtr<Shape> gifImage = builder->InsertImage(ImageDir + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(ImageDir + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(ArtifactsDir + u"InsertGif.docx");
```


Shows how to insert a shape with an image into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two locations where the document builder's "InsertShape" method
// can source the image that the shape will display.
// 1 -  Pass a local file system filename of an image file:
builder->Write(u"Image from local file: ");
builder->InsertImage(ImageDir + u"Logo.jpg");
builder->Writeln();

// 2 -  Pass a URL which points to an image.
builder->Write(u"Image from a URL: ");
builder->InsertImage(ImageUrl);
builder->Writeln();

doc->Save(ArtifactsDir + u"Image.FromUrl.docx");
```


Shows how to insert a floating image to the center of a page. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(HorizontalAlignment::Center);
shape->set_VerticalAlignment(VerticalAlignment::Center);

doc->Save(ArtifactsDir + u"Image.CreateFloatingPageCenter.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts an image from a file or URL at the specified position and size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The file that contains the image. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | double | Distance in points from the origin to the left side of the image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | double | Distance in points from the origin to the top side of the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the image. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// There are two ways of using a document builder to source an image and then insert it as a floating shape.
// 1 -  From a file in the local file system:
builder->InsertImage(ImageDir + u"Transparent background logo.png", RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 0.0,
                     200.0, 200.0, WrapType::Square);

// 2 -  From a URL:
builder->InsertImage(ImageUrl, RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertFloatingImage.docx");
```


Shows how to insert an image from the local file system into a document while preserving its dimensions. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// The InsertImage method creates a floating shape with the passed image in its image data.
// We can specify the dimensions of the shape can be passing them to this method.
SharedPtr<Shape> imageShape = builder->InsertImage(ImageDir + u"Logo.jpg", RelativeHorizontalPosition::Margin, 0.0, RelativeVerticalPosition::Margin,
                                                   0.0, -1.0, -1.0, WrapType::Square);

// Passing negative values as the intended dimensions will automatically define
// the shape's dimensions based on the dimensions of its image.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Shows how to insert an image from the local file system into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are three ways of inserting an image from a local system filename.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder->InsertImage(ImageDir + u"Logo.jpg");

builder->InsertBreak(BreakType::PageBreak);

// 2 -  Inline shape with custom dimensions:
builder->InsertImage(ImageDir + u"Transparent background logo.png", ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

builder->InsertBreak(BreakType::PageBreak);

// 3 -  Floating shape with custom dimensions:
builder->InsertImage(ImageDir + u"Windows MetaFile.wmf", RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0,
                     100.0, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Inserts an inline image from a file or URL into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The file that contains the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an image from the local file system into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are three ways of inserting an image from a local system filename.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder->InsertImage(ImageDir + u"Logo.jpg");

builder->InsertBreak(BreakType::PageBreak);

// 2 -  Inline shape with custom dimensions:
builder->InsertImage(ImageDir + u"Transparent background logo.png", ConvertUtil::PixelToPoint(250), ConvertUtil::PixelToPoint(144));

builder->InsertBreak(BreakType::PageBreak);

// 3 -  Floating shape with custom dimensions:
builder->InsertImage(ImageDir + u"Windows MetaFile.wmf", RelativeHorizontalPosition::Margin, 100.0, RelativeVerticalPosition::Margin, 100.0, 200.0,
                     100.0, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, double, double) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, double width, double height)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
