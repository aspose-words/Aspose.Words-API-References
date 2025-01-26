---
title: Aspose::Words::LowCode::Comparer class
linktitle: Comparer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Comparer class. Provides methods intended to compare documents in C++.'
type: docs
weight: 500
url: /cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Provides methods intended to compare documents.

```cpp
class Comparer
```

## Methods

| Method | Description |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | Compares two documents and saves the differences to the specified output file, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Compares two documents and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents with additional options and saves the differences to the specified output file, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Compares two documents loaded from streams and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions. |
| [Comparer](./comparer/)() |  |
## See Also

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
