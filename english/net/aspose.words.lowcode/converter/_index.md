---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words for .NET
description: Effortlessly convert various document types with Aspose.Words.LowCode.Converter. Simplify your workflow using just one line of code for seamless integration.
type: docs
weight: 4260
url: /net/aspose.words.lowcode/converter/
---
## Converter class

Represents a group of methods intended to convert a variety of different types of documents using a single line of code.

```csharp
public class Converter : Processor
```

## Methods

| Name | Description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | Creates new instance of the converter processor. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | Creates new instance of the converter processor. |
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
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | Converts the given input document into the output document using specified input output file names and its extensions. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the given input document into a single output document using specified input and output streams. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Converts the given input document into a single output document using specified input and output streams. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the given input document into the output document using specified input output file names and the final document format. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Converts the given input document into the output document using specified input output file names and save options. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Converts the given input document into a single output document using specified input and output streams. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Converts the given input document into the output document using specified input output file names its load/save options. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the pages of the specified document to images using the specified save options and returns an array of streams containing the images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Converts the pages of the specified document to images in the specified format and returns an array of streams containing the images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the pages of the specified input stream to images using the specified save options and returns an array of streams containing the images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the pages of the specified input stream to images in the specified format and returns an array of streams containing the images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the pages of the specified input file to images using the specified save options and returns an array of streams containing the images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the pages of the specified input file to images in the specified format and returns an array of streams containing the images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the pages of the specified input stream to images using the provided load and save options, and returns an array of streams containing the images. |

## Remarks

The specified input and output files or streams, along with the desired save format, are used to convert the given input document of the one format into the output document of the other specified format.

The convert functionality supports over 35+ different file formats.

The [`ConvertToImages`](./converttoimages/) group of methods are designed to transform documents into images, with each page being converted into a separate image file. These methods also convert PDF documents directly to fixed-page formats without loading them into the document model, which enhances both performance and accuracy.

With [`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), you can specify a particular set of pages to convert into images.

### See Also

* class [Processor](../processor/)
* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
