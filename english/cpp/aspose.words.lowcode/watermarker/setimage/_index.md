---
title: Aspose::Words::LowCode::Watermarker::SetImage method
linktitle: SetImage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Watermarker::SetImage method. Adds an image watermark into the document from streams with options in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Image that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Image stream that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Image that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Image stream that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document with options and specified save format.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| watermarkImageFileName | const System::String\& | Image that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document with options and specified save format.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options=System::ExplicitCast<Aspose::Words::ImageWatermarkOptions>(nullptr))
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| watermarkImageFileName | const System::String\& | Image that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Adds an image watermark into the document.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| watermarkImageFileName | const System::String\& | Image that is displayed as a watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Adds an image watermark into the document with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| watermarkImageFileName | const System::String\& | Image that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Defines additional options for the image watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
