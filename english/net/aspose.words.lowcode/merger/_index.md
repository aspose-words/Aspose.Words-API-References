---
title: Merger Class
linktitle: Merger
articleTitle: Merger
second_title: Aspose.Words for .NET
description: Effortlessly merge diverse document types into one with Aspose.Words.LowCode.Merger class. Streamline your workflow and enhance productivity today!
type: docs
weight: 4330
url: /net/aspose.words.lowcode/merger/
---
## Merger class

Represents a group of methods intended to merge a variety of different types of documents into a single output document.

```csharp
public class Merger : Processor
```

## Methods

| Name | Description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/merger/create/#create)() | Creates new instance of the mail merger processor. |
| static [Create](../../aspose.words.lowcode/merger/create/#create_1)(*[MergerContext](../mergercontext/)*) | Creates new instance of the mail merger processor. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Execute the processor action. |
| [Execute](../../aspose.words.lowcode/processor/execute/)(*CancellationToken*) | Execute the processor action allowing canceling document processing task using specified cancellation token. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/)(*string*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [To](../../aspose.words.lowcode/processor/to/)(*string*) | Specifies output file for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output file for the processor. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output file for the processor. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge)(*Document[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_2)(*Stream[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_8)(*string, string[]*) | Merges the given input documents into a single output document using specified input and output file names using KeepSourceFormatting. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_4)(*string[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_6)(*Stream, Stream[], [SaveFormat](../../aspose.words/saveformat/)*) | Merges the given input documents into a single output document using specified input output streams and the final document format. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_1)(*Stream[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_3)(*string[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single document and returns [`Document`](../../aspose.words/document/) instance of the final document. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_7)(*Stream, Stream[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output streams and save options. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_10)(*string, string[], [SaveFormat](../../aspose.words/saveformat/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output file names and the final document format. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_11)(*string, string[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output file names and save options. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_5)(*Stream, Stream[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output streams and save options. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_9)(*string, string[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output file names and save options. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages)(*Stream[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input document streams into a single output document using specified image save options. Renders the output to images. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages_1)(*string[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Merges the given input documents into a single output document using specified input output file names and save options. Renders the output to images. |

## Remarks

The specified input and output files or streams, along with the desired merge and save options, are used to merge the given input documents into a single output document.

The merging functionality supports over 35 different file formats.

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* class [Processor](../processor/)
* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
