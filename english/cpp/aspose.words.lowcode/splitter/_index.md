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
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Removes empty pages from the document and saves the output. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Removes empty pages from the document and saves the output in the specified format. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Removes empty pages from the document and saves the output in the specified format. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Removes empty pages from the document and saves the output. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Removes empty pages from the document and saves the output in the specified format. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Removes empty pages from the document and saves the output in the specified format. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\&) | Splits the document into parts. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\&) | Splits the document into parts. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::Splitting::SplitOptions\>\&) | Splits the document into parts. |
| [Splitter](./splitter/)() |  |
## See Also

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
