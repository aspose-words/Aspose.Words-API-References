---
title: "Aspose::Words::LowCode::Comparer::Compare method"
linktitle: "比较"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Comparer::Compare 方法。比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，在 C++ 中生成一系列编辑和格式修订的更改。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | 原始文档。 |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | 修改后的文档。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 输出的保存格式。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | 原始文档。 |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | 修改后的文档。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 输出的保存格式。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) 比较选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | 原始文档。 |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | 修改后的文档。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 输出的保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | 原始文档。 |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | 修改后的文档。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 输出的保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) 比较选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 输出的保存格式。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 输出的保存格式。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) 比较选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 输出的保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 输出的保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) 比较选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


比较两个文档并使用附加选项，将差异保存到指定的输出文件中，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| outputFileName | const System::String\& | 输出文件名。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


比较两个文档并使用附加选项，将差异保存到指定的输出文件中，以编辑和格式修订的数量形式生成更改。

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| outputFileName | const System::String\& | 输出文件名。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) 比较选项。 |
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
