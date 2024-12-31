---
title: Aspose::Words::LowCode::Splitter::Split method
linktitle: Split
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Splitter::Split method. Splits the document into parts in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\&) method


Splits the document into parts.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::Splitting::SplitOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\& | [Document](../../../aspose.words/document/) split options. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../../aspose.words.lowcode.splitting/splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\&) method


Splits the document into parts.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::Splitting::SplitOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\& | [Document](../../../aspose.words/document/) split options. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../../aspose.words.lowcode.splitting/splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\&) method


Splits the document into parts.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::Splitting::SplitOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| options | const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\& | [Document](../../../aspose.words/document/) split options. |

## See Also

* Class [SplitOptions](../../../aspose.words.lowcode.splitting/splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
