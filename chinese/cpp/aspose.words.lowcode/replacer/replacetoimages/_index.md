---
title: "Aspose::Words::LowCode::Replacer::ReplaceToImages 方法"
linktitle: "ReplaceToImages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Replacer::ReplaceToImages 方法。将输入文件中所有匹配指定正则表达式模式的出现替换为替换字符串，并在 C++ 中将输出渲染为图像。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.lowcode/replacer/replacetoimages/
---
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入文件流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入文件流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入文件流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入文件流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
