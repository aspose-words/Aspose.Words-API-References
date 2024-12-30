---
title: Aspose::Words::LowCode::Splitter::RemoveBlankPages method
linktitle: RemoveBlankPages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Splitter::RemoveBlankPages method. Removes empty pages from the document and saves the output in the specified format in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.lowcode/splitter/removeblankpages/
---
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Removes empty pages from the document and saves the output in the specified format.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |

### ReturnValue

List of page numbers has been considered as blank and removed.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&) method


Removes empty pages from the document and saves the output.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |

### ReturnValue

List of page numbers has been considered as blank and removed.

## See Also

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Removes empty pages from the document and saves the output in the specified format.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |

### ReturnValue

List of page numbers has been considered as blank and removed.

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
