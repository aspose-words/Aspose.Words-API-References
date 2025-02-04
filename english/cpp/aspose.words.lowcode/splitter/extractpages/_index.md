---
title: Aspose::Words::LowCode::Splitter::ExtractPages method
linktitle: ExtractPages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Splitter::ExtractPages method. Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | The input stream. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | The output stream. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| startPageIndex | int32_t | The zero-based index of the first page to extract. |
| pageCount | int32_t | Number of pages to be extracted. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| saveFormat | Aspose::Words::SaveFormat | The save format. |
| startPageIndex | int32_t | The zero-based index of the first page to extract. |
| pageCount | int32_t | Number of pages to be extracted. |

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Extracts a specified range of pages from a document file and saves the extracted pages to a new file. The output file format is determined by the extension of the output file name.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | The input file name. |
| outputFileName | const System::String\& | The output file name. |
| startPageIndex | int32_t | The zero-based index of the first page to extract. |
| pageCount | int32_t | Number of pages to be extracted. |

## See Also

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
