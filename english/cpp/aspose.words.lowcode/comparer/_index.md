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
class Comparer : public Aspose::Words::LowCode::Processor
```

## Methods

| Method | Description |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents with additional options and saves the differences to the specified output file, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image. |
| static [Create](./create/)() | Creates new instance of the converter processor. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Creates new instance of the comparer processor. |
| [Execute](../processor/execute/)() | Execute the processor action. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifies input document for processing. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifies input document for processing. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Specifies output file for the processor. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Specifies output file for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Specifies output stream for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Specifies output stream for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## See Also

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
