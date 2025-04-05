---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words for .NET
description: Effortlessly split documents with Aspose.Words.LowCode.Splitter class. Utilize versatile methods for precise document management and enhanced workflow efficiency.
type: docs
weight: 4410
url: /net/aspose.words.lowcode/splitter/
---
## Splitter class

Provides methods intended to split the documents into parts using different criteria.

```csharp
public class Splitter : Processor
```

## Methods

| Name | Description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Creates new instance of the splitter processor. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Execute the processor action. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output file for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output file for the processor. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file. The output file format is determined by the extension of the output file name. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Removes blank pages from a document provided in an input stream and saves the updated document to an output stream in the specified save format. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Removes blank pages from a document provided in an input stream and saves the updated document to an output stream in the specified save format. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files. The output file format is determined by the extension of the output file name. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format. |

### See Also

* class [Processor](../processor/)
* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
