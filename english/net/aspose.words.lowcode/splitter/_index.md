---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words for .NET
description: Aspose.Words.LowCode.Splitter class. Provides methods intended to split the documents into parts using different criteria in C#.
type: docs
weight: 4260
url: /net/aspose.words.lowcode/splitter/
---
## Splitter class

Provides methods intended to split the documents into parts using different criteria.

```csharp
public static class Splitter
```

## Methods

| Name | Description |
| --- | --- |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, int, int*) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file. The output file format is determined by the extension of the output file name. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*string, string*) | Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Removes blank pages from a document provided in an input stream and saves the updated document to an output stream in the specified save format. Returns a list of page numbers that were removed. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../../aspose.words.lowcode.splitting/splitoptions/)*) | Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*string, string, [SplitOptions](../../aspose.words.lowcode.splitting/splitoptions/)*) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files. The output file format is determined by the extension of the output file name. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../../aspose.words.lowcode.splitting/splitoptions/)*) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format. |

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
