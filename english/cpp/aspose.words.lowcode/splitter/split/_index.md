---
title: Aspose::Words::LowCode::Splitter::Split method
linktitle: Split
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Splitter::Split method. Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) split options. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method




```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) split options. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Splits a document into multiple parts based on the specified split options and saves the resulting parts to files. The output file format is determined by the extension of the output file name.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) split options. |

## See Also

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method




```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
