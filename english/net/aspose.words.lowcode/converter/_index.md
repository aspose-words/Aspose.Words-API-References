---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words for .NET
description: Aspose.Words.LowCode.Converter class. Represents a group of methods intended to convert a variety of different types of documents using a single line of code in C#.
type: docs
weight: 4190
url: /net/aspose.words.lowcode/converter/
---
## Converter class

Represents a group of methods intended to convert a variety of different types of documents using a single line of code.

```csharp
public static class Converter
```

## Methods

| Name | Description |
| --- | --- |
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
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_8)(*string, string*) | Converts the pages of the specified input file to image files. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the pages of the specified input stream to images using the provided load and save options, and returns an array of streams containing the images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_10)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the pages of the specified input file to image files using the specified save options. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_9)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the pages of the specified input file to image files in the specified format. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_7)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the pages of the specified input file to image files using the provided load and save options. |

## Remarks

The specified input and output files or streams, along with the desired save format, are used to convert the given input document of the one format into the output document of the other specified format.

The convert functionality supports over 35+ different file formats.

The [`ConvertToImages`](./converttoimages/) group of methods are designed to transform documents into images, with each page being converted into a separate image file. These methods also convert PDF documents directly to fixed-page formats without loading them into the document model, which enhances both performance and accuracy.

With [`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), you can specify a particular set of pages to convert into images.

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
