---
title: Merger Class
linktitle: Merger
articleTitle: Merger
second_title: Aspose.Words for .NET
description: Aspose.Words.LowCode.Merger class. Represents a group of methods intended to merge a variety of different types of documents into a single output document in C#.
type: docs
weight: 4220
url: /net/aspose.words.lowcode/merger/
---
## Merger class

Represents a group of methods intended to merge a variety of different types of documents into a single output document.

```csharp
public static class Merger
```

## Methods

| Name | Description |
| --- | --- |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge)(*Document[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_2)(*Stream[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_8)(*string, string[]*) | Merges the given input documents into a single output document using specified input and output file names. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_4)(*string[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_6)(*Stream, Stream[], [SaveFormat](../../aspose.words/saveformat/)*) | Merges the given input documents into a single output document using specified input output streams and the final document format. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_1)(*Stream[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_3)(*string[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_7)(*Stream, Stream[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output streams and save options. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_10)(*string, string[], [SaveFormat](../../aspose.words/saveformat/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output file names and the final document format. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_11)(*string, string[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output file names and save options. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_5)(*Stream, Stream[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output streams and save options. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_9)(*string, string[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output file names and save options. |

## Remarks

The specified input and output files or streams, along with the desired merge and save options, are used to merge the given input documents into a single output document.

The merging functionality supports over 35 different file formats.

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
