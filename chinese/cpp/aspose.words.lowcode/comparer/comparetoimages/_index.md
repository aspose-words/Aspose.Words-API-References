---
title: "Aspose::Words::LowCode::Comparer::CompareToImages method"
linktitle: "CompareToImages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Comparer::CompareToImages 方法。比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页，以图像形式呈现（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.lowcode/comparer/comparetoimages/
---
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | 原始文档。 |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | 修改后的文档。 |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 输出的图像保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | 原始文档。 |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | 修改后的文档。 |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 输出的图像保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) 比较选项。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 输出的图像保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| v1 | const System::String\& | 原始文档。 |
| v2 | const System::String\& | 修改后的文档。 |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 输出的图像保存选项。 |
| 作者 | const System::String\& | 用于修订的作者缩写。 |
| dateTime | System::DateTime | 用于修订的日期和时间。 |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) 比较选项。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
