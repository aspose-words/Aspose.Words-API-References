---
title: SetImage
second_title: Aspose.Words for C++ API Reference
description: Adds Image watermark into the document.
type: docs
weight: 27
url: /cpp/aspose.words/watermark/setimage/
---
## Watermark.SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Adds Image watermark into the document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Image that is displayed as a watermark. |


## Watermark.SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


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
auto doc = MakeObject<Document>();

// Modify the image watermark's appearance with an ImageWatermarkOptions object,
// then pass it while creating a watermark from an image file.
auto imageWatermarkOptions = MakeObject<ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg"), imageWatermarkOptions);

doc->Save(ArtifactsDir + u"Document.ImageWatermark.docx");
```

## Watermark.SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds Image watermark into the document.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| imagePath | const System::String\& | Path to the image file that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |


