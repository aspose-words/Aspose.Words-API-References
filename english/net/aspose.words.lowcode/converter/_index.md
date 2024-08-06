---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words for .NET
description: Aspose.Words.LowCode.Converter class. Represents a group of methods intended to convert a variety of different types of documents using a single line of code in C#.
type: docs
weight: 4030
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
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*string, string*) | Converts the given input document into the output document using specified input output file names and its extensions. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the given input document into a single output document using specified input and output streams. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Converts the given input document into a single output document using specified input and output streams. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the given input document into the output document using specified input output file names and the final document format. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Converts the given input document into the output document using specified input output file names and save options. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the document pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Converts the document pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the input stream pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the input stream pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the input file pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the input file pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, string*) | Converts the input file pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_8)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Converts the input file pages to images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Converts the input file pages to images. |

## Remarks

The specified input and output files or streams, along with the desired save format, are used to convert the given input document of the one format into the output document of the other specified format.

The convert functionality supports over 35+ different file formats.

The [`ConvertToImages`](./converttoimages/) group of methods are designed to transform documents into images, with each page being converted into a separate image file. These methods also convert PDF documents directly to fixed-page formats without loading them into the document model (using our pdf2word plugin), which enhances both performance and accuracy.

With [`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), you can specify a particular set of pages to convert into images.

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
