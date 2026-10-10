---
title: "Aspose::Words::LowCode::Converter::ConvertToImages 方法"
linktitle: "转换为图像"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Converter::ConvertToImages 方法。将指定文档的页面转换为指定格式的图像，并在 C++ 中返回包含这些图像的流数组。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


将指定文档的页面转换为指定格式的图像，并返回包含这些图像的流数组。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::Document\>\& | 输入文档。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。仅允许图像保存格式。 |

### ReturnValue

返回图像流数组。流应由最终用户释放。

## 另见

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


使用指定的保存选项，将指定文档的页面转换为图像，并返回包含这些图像的流数组。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::Document\>\& | 输入文档。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 图像保存选项。 |

### ReturnValue

返回图像流数组。流应由最终用户释放。

## 另见

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


将指定输入流的页面转换为指定格式的图像，并返回包含这些图像的流数组。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。仅允许图像保存格式。 |

### ReturnValue

返回图像流数组。流应由最终用户释放。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


使用提供的加载和保存选项，将指定输入流的页面转换为图像，并返回包含这些图像的流数组。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | 输入文档的加载选项。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 图像保存选项。 |

### ReturnValue

返回图像流数组。流应由最终用户释放。

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


使用指定的保存选项，将指定输入流的页面转换为图像，并返回包含这些图像的流数组。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 图像保存选项。 |

### ReturnValue

返回图像流数组。流应由最终用户释放。

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


将指定输入文件的页面转换为指定格式的图像，并返回包含这些图像的流数组。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。仅允许图像保存格式。 |

### ReturnValue

返回图像流数组。流应由最终用户释放。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


使用提供的加载和保存选项，将指定输入文件的页面转换为图像文件。

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | 输入文档的加载选项。 |
| outputFile | const System::String\& | 用于根据规则 "outputFile_pageIndex.extension" 生成页面图像文件名的输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 图像保存选项。 |

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


使用指定的保存选项，将指定输入文件的页面转换为图像，并返回包含这些图像的流数组。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 图像保存选项。 |

### ReturnValue

返回图像流数组。流应由最终用户释放。

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


将指定输入文件的页面转换为图像文件。

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| outputFile | const System::String\& | 用于根据规则 "outputFile_pageIndex.extension" 生成页面图像文件名的输出文件名。 |

## 另见

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


将指定输入文件的页面转换为指定格式的图像文件。

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| outputFile | const System::String\& | 用于根据规则 "outputFile_pageIndex.extension" 生成页面图像文件名的输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。仅允许图像保存格式。 |

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


使用指定的保存选项，将指定输入文件的页面转换为图像文件。

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFile | const System::String\& | 输入文件名。 |
| outputFile | const System::String\& | 用于根据规则 "outputFile_pageIndex.extension" 生成页面图像文件名的输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 图像保存选项。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
