---
title: Aspose::Words::LowCode::Splitter class
linktitle: Splitter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Splitter class. Provides methods intended to split the documents into parts using different criteria in C++.'
type: docs
weight: 1500
url: /cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Provides methods intended to split the documents into parts using different criteria.

```cpp
class Splitter
```

## Methods

| Method | Description |
| --- | --- |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file. The output file format is determined by the extension of the output file name. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Removes blank pages from a document provided in an input stream and saves the updated document to an output stream in the specified save format. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Removes blank pages from a document provided in an input stream and saves the updated document to an output stream in the specified save format. Returns a list of page numbers that were removed. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files. The output file format is determined by the extension of the output file name. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format. |
| [Splitter](./splitter/)() |  |
## See Also

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
