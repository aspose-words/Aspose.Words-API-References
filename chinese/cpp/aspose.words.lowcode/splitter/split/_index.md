---
title: "Aspose::Words::LowCode::Splitter::Split 方法"
linktitle: "拆分"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Splitter::Split 方法。根据指定的拆分选项，将文档从输入流拆分为多个部分，并以指定的保存格式返回包含流的数组（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


从输入流中的文档根据指定的拆分选项拆分为多个部分，并以指定的保存格式将生成的部分作为流数组返回。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) 拆分选项。 |

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


从输入流中的文档根据指定的拆分选项拆分为多个部分，并以指定的保存格式将生成的部分作为流数组返回。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) 拆分选项。 |

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


根据指定的拆分选项将文档拆分为多个部分，并以指定的保存格式将生成的部分保存为文件。

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 用于根据规则 "outputFile_partIndex.extension" 生成文档部件文件名的输出文件名 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) 拆分选项。 |

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


根据指定的拆分选项将文档拆分为多个部分，并将生成的部分保存为文件。输出文件格式由输出文件名的扩展名决定。

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 用于根据规则 "outputFile_partIndex.extension" 生成文档部件文件名的输出文件名 |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) 拆分选项。 |

## 另见

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


根据指定的拆分选项将文档拆分为多个部分，并以指定的保存格式将生成的部分保存为文件。

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 用于根据规则 "outputFile_partIndex.extension" 生成文档部件文件名的输出文件名 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) 拆分选项。 |

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
