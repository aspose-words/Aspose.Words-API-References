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
class Merger
```

## Methods

| Method | Description |
| --- | --- |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Merges the given input documents into a single output document using specified input and output file names. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output file names and the final document format. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output file names and save options. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) |  |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Merges the given input documents into a single output document using specified input output streams and the final document format. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single output document using specified input output streams and save options. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
| [Merger](./merger/)() |  |
## Remarks


The specified input and output files or streams, along with the desired merge and save options, are used to merge the given input documents into a single output document.

The merging functionality supports over 35 different file formats. 
## See Also

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
