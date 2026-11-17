---
title: Aspose::Words::LowCode::Watermarker::SetText method
linktitle: SetText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Watermarker::SetText method. Adds a text watermark into the document from streams with options in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.lowcode/watermarker/settext/
---
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) method


Adds a text watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds a text watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Adds a text watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds a text watermark into the document from streams with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Adds a text watermark into the document with options and specified save format.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds a text watermark into the document with options and specified save format.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Adds a text watermark into the document with options and specified save format.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds a text watermark into the document with options and specified save format.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&) method


Adds a text watermark into the document.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Adds a text watermark into the document with options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| watermarkText | const System::String\& | Text that is displayed as a watermark. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Defines additional options for the text watermark. |
## Remarks


If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## See Also

* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
