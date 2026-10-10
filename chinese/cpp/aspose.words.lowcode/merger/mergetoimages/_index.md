---
title: "Aspose::Words::LowCode::Merger::MergeToImages 方法"
linktitle: "MergeToImages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Merger::MergeToImages 方法。将给定的输入文档流合并为单个输出文档，使用指定的图像保存选项。将在 C++ 中将输出渲染为图像。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


使用指定的图像保存选项将给定的输入文档流合并为单个输出文档。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | 输入文件流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | 指定如何合并冲突的格式。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | 输入文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | 指定如何合并冲突的格式。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
