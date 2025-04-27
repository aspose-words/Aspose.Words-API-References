---
title: Aspose::Words::LowCode::Watermarker::SetWatermarkToImages method
linktitle: SetWatermarkToImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Watermarker::SetWatermarkToImages method. Adds an image watermark into the document with options. Renders the output to images in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document with options. Renders the output to images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The save options. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Image stream that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds a text watermark into the document with options. Renders the output to images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::TextWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input file stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The save options. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document with options. Renders the output to images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::ArrayPtr<uint8_t> &watermarkImageBytes, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The save options. |
| watermarkImageBytes | const System::ArrayPtr\<uint8_t\>\& | Image bytes that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds a text watermark into the document with options. Renders the output to images.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::TextWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | The save options. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
