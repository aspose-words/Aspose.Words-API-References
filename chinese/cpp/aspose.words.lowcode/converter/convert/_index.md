---
title: "Aspose::Words::LowCode::Converter::Convert 方法"
linktitle: "转换"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Converter::Convert 方法。将给定的输入文档使用指定的输入和输出流在 C++ 中转换为单个输出文档。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.lowcode/converter/convert/
---
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


使用指定的输入和输出流，将给定的输入文档转换为单个输出文档。

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | 输入文档的加载选项。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


使用指定的输入和输出流，将给定的输入文档转换为单个输出文档。

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


使用指定的输入和输出流，将给定的输入文档转换为单个输出文档。

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


使用指定的输入输出文件名及其加载/保存选项，将给定的输入文档转换为输出文档。

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | 输入文档的加载选项。 |
| outputFile | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&) method


使用指定的输入输出文件名及其扩展名，将给定的输入文档转换为输出文档。

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| outputFile | const System::String\& | 输出文件名。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


使用指定的输入输出文件名和最终文档格式，将给定的输入文档转换为输出文档。

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| outputFile | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


使用指定的输入输出文件名和保存选项，将给定的输入文档转换为输出文档。

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| outputFile | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
