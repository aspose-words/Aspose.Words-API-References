---
title: "Aspose::Words::LowCode::Splitter::ExtractPages 方法"
linktitle: "ExtractPages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Splitter::ExtractPages 方法。提取文档流中指定范围的页面，并使用指定的保存格式将提取的页面保存到输出流中（C++）。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到输出流中。

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| startPageIndex | int32_t | 要提取的第一页的零基索引。 |
| pageCount | int32_t | 要提取的页面数量。 |

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到输出流中。

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| startPageIndex | int32_t | 要提取的第一页的零基索引。 |
| pageCount | int32_t | 要提取的页面数量。 |

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到新文件中。

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| startPageIndex | int32_t | 要提取的第一页的零基索引。 |
| pageCount | int32_t | 要提取的页面数量。 |

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到新文件中。

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| startPageIndex | int32_t | 要提取的第一页的零基索引。 |
| pageCount | int32_t | 要提取的页面数量。 |

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


从文档文件中提取指定范围的页面，并将提取的页面保存到新文件中。输出文件格式由输出文件名的扩展名决定。

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| startPageIndex | int32_t | 要提取的第一页的零基索引。 |
| pageCount | int32_t | 要提取的页面数量。 |

## 另见

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
