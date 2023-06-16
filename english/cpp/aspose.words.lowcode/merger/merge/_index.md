---
title: Aspose::Words::LowCode::Merger::Merge method
linktitle: Merge
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Merger::Merge method. Merges the given input documents into a single document and returns Document instance of the final document in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.lowcode/merger/merge/
---
## Merger::Merge(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.

```cpp
static System::SharedPtr<Aspose::Words::Document> Aspose::Words::LowCode::Merger::Merge(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | The input streams. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Specifies how to merge formatting that clashes. |

## See Also

* Class [Document](../../../aspose.words/document/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::Merge(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.

```cpp
static System::SharedPtr<Aspose::Words::Document> Aspose::Words::LowCode::Merger::Merge(const System::ArrayPtr<System::String> &inputFiles, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | The input file names. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Specifies how to merge formatting that clashes. |

## See Also

* Class [Document](../../../aspose.words/document/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::Merge(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) method


Merges the given input documents into a single output document using specified input output streams and the final document format.

```cpp
static void Aspose::Words::LowCode::Merger::Merge(const System::SharedPtr<System::IO::Stream> &outputStream, const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | The input streams. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::Merge(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Merges the given input documents into a single output document using specified input output streams and save options.

```cpp
static void Aspose::Words::LowCode::Merger::Merge(const System::SharedPtr<System::IO::Stream> &outputStream, const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | The input streams. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Specifies how to merge formatting that clashes. |

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::Merge(const System::String\&, const System::ArrayPtr\<System::String\>\&) method


Merges the given input documents into a single output document using specified input and output file names.

```cpp
static void Aspose::Words::LowCode::Merger::Merge(const System::String &outputFile, const System::ArrayPtr<System::String> &inputFiles)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | const System::String\& | The output file name. |
| inputFiles | const System::ArrayPtr\<System::String\>\& | The input file names. |
## Remarks


By default [KeepSourceFormatting](../../mergeformatmode/) is used.

## See Also

* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::Merge(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) method


Merges the given input documents into a single output document using specified input output file names and the final document format.

```cpp
static void Aspose::Words::LowCode::Merger::Merge(const System::String &outputFile, const System::ArrayPtr<System::String> &inputFiles, Aspose::Words::SaveFormat saveFormat, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | const System::String\& | The output file name. |
| inputFiles | const System::ArrayPtr\<System::String\>\& | The input file names. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Specifies how to merge formatting that clashes. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::Merge(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Merges the given input documents into a single output document using specified input output file names and save options.

```cpp
static void Aspose::Words::LowCode::Merger::Merge(const System::String &outputFile, const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | const System::String\& | The output file name. |
| inputFiles | const System::ArrayPtr\<System::String\>\& | The input file names. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | The save options. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Specifies how to merge formatting that clashes. |

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
