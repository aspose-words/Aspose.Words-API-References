---
title: "Aspose::Words::LowCode::Watermarker::SetImage 方法"
linktitle: "SetImage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Watermarker::SetImage 方法。使用选项从流向文档添加图像水印，在 C++ 中。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | 作为水印显示的图像。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | 作为水印显示的图像。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | 作为水印显示的图像流。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | 作为水印显示的图像流。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | 作为水印显示的图像。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | 作为水印显示的图像。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | 作为水印显示的图像流。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


使用选项从流向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | 作为水印显示的图像流。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


使用选项和指定的保存格式向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| watermarkImageFileName | const System::String\& | 作为水印显示的图像。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


使用选项和指定的保存格式向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| watermarkImageFileName | const System::String\& | 作为水印显示的图像。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


使用选项和指定的保存格式向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| watermarkImageFileName | const System::String\& | 作为水印显示的图像。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


使用选项和指定的保存格式向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| watermarkImageFileName | const System::String\& | 作为水印显示的图像。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| watermarkImageFileName | const System::String\& | 作为水印显示的图像。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


使用选项向文档添加图像水印。

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| watermarkImageFileName | const System::String\& | 作为水印显示的图像。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
