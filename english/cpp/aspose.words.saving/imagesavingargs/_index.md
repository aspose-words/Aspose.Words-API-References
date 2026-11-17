---
title: Aspose::Words::Saving::ImageSavingArgs class
linktitle: ImageSavingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSavingArgs class. Provides data for the ImageSaving() event. To learn more, visit the  documentation article in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Provides data for the [ImageSaving()](../iimagesavingcallback/imagesaving/) event. To learn more, visit the [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) documentation article.

```cpp
class ImageSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Gets the [ShapeBase](../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape that is about to be saved. |
| [get_Document](./get_document/)() | Gets the document object that is currently being saved. |
| [get_ImageFileName](./get_imagefilename/)() const | Gets or sets the file name (without path) where the image will be saved to. |
| [get_ImageStream](./get_imagestream/)() const | Allows to specify the stream where the image will be saved to. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Returns **true** if the current image is available for export. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Setter for [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Setter for [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Remarks


By default, when Aspose.Words saves a document to HTML, it saves each image into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) and [IsImageAvailable](./get_isimageavailable/) properties.

To save images into streams instead of files, use the [ImageStream](./get_imagestream/) property. 
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
