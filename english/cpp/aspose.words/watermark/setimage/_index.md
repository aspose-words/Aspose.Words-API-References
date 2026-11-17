---
title: Aspose::Words::Watermark::SetImage method
linktitle: SetImage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Watermark::SetImage method. Adds Image watermark into the document in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Adds Image watermark into the document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Image that is displayed as a watermark. |

## Examples



Shows how to create a watermark from an image in the local file system. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modify the image watermark's appearance with an ImageWatermarkOptions object,
// then pass it while creating a watermark from an image file.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// We have a different options to insert image.
// Use on of the following methods to add image watermark.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## See Also

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds Image watermark into the document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Image that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |

## Examples



Shows how to create a watermark from an image in the local file system. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modify the image watermark's appearance with an ImageWatermarkOptions object,
// then pass it while creating a watermark from an image file.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// We have a different options to insert image.
// Use on of the following methods to add image watermark.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## See Also

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds Image watermark into the document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | The stream containing the image data that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |

## Examples



Shows how to create a watermark from an image stream. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modify the image watermark's appearance with an ImageWatermarkOptions object,
// then pass it while creating a watermark from an image file.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## See Also

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds Image watermark into the document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| imagePath | const System::String\& | Path to the image file that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |

## Examples



Shows how to create a watermark from an image in the local file system. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modify the image watermark's appearance with an ImageWatermarkOptions object,
// then pass it while creating a watermark from an image file.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// We have a different options to insert image.
// Use on of the following methods to add image watermark.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## See Also

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
