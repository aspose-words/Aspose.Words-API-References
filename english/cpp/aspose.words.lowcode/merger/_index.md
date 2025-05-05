---
title: Aspose::Words::LowCode::Merger class
linktitle: Merger
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::Merger class. Represents a group of methods intended to merge a variety of different types of documents into a single output document in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.lowcode/merger/
---
## Merger class


Represents a group of methods intended to merge a variety of different types of documents into a single output document.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Methods

| Method | Description |
| --- | --- |
| static [Create](./create/)() | Creates new instance of the mail merger processor. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Creates new instance of the mail merger processor. |
| [Execute](../processor/execute/)() | Execute the processor action. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifies input document for processing. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Specifies input document for processing. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Merges the given input documents into a single output document using specified input and output file names using [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output file names and the final document format. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output file names and save options. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output file names and save options. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Merges the given input documents into a single output document using specified input output streams and the final document format. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output streams and save options. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output streams and save options. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output file names and save options. Renders the output to images. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input document streams into a single output document using specified image save options. Renders the output to images. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Specifies output file for the processor. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Specifies output file for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Specifies output stream for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Specifies output stream for the processor. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Remarks


The specified input and output files or streams, along with the desired merge and save options, are used to merge the given input documents into a single output document.

The merging functionality supports over 35 different file formats. 
## See Also

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
