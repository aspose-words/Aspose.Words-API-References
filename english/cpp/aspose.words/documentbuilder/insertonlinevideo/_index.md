---
title: Aspose::Words::DocumentBuilder::InsertOnlineVideo method
linktitle: InsertOnlineVideo
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertOnlineVideo method. Inserts an online video object into the document and scales it to the specified size in C++.'
type: docs
weight: 43000
url: /cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts an online video object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | The URL to the video. |
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

Insertion of online video from the following resources is supported:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



If your online video is not displaying correctly, use [InsertOnlineVideo()](../), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts an online video object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | The URL to the video. |
| videoEmbedCode | const System::String\& | The embed code for the video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | The thumbnail image bytes. |
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

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Inserts an online video object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | The URL to the video. |
| videoEmbedCode | const System::String\& | The embed code for the video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | The thumbnail image bytes. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Inserts an online video object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | const System::String\& | The URL to the video. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

Insertion of online video from the following resources is supported:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



If your online video is not displaying correctly, use [InsertOnlineVideo()](../), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
