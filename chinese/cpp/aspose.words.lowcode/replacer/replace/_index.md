---
title: "Aspose::Words::LowCode::Replacer::Replace 方法"
linktitle: "Replace"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Replacer::Replace 方法。使用正则表达式在输入流中将所有匹配指定字符字符串模式的出现替换为替换字符串，并使用指定的保存格式和其他选项在 C++ 中进行处理。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则仅将输出的第一页保存到指定的流中。

如果输出格式是 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流中。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveFormat | Aspose::Words::SaveFormat | 保存格式。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 保存选项。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | const System::String\& | 输入文件名。 |
| outputFileName | const System::String\& | 输出文件名。 |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则生成每个部分的文件名：outputFile_partIndex.extension。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

## 另见

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
