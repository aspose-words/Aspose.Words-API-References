---
title: Converter class
linktitle: Converter class
articleTitle: Converter class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Converter class. Represents a group of methods intended to convert a variety of different types of documents using a single line of code."
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/converter/
---

## Converter class

Represents a group of methods intended to convert a variety of different types of documents using a single line of code.


### Remarks

The specified input and output files or streams, along with the desired save format,
are used to convert the given input document of the one format into the output document
of the other specified format.

The convert functionality supports over 35+ different file formats.

The [Converter.convert_to_images()](./convert_to_images/#str_saveformat) group of methods are designed to transform documents into images,
with each page being converted into a separate image file. These methods also convert PDF documents directly to fixed-page formats
without loading them into the document model, which enhances both performance and accuracy.

With [ImageSaveOptions.page_set](../../aspose.words.saving/imagesaveoptions/page_set/), you can specify a particular set of pages to convert into images.




**Inheritance:** [Converter](./) → [Processor](../processor/)

### Methods

| Name | Description |
| --- | --- |
|[ convert(input_file, output_file)](./convert/#str_str) | Converts the given input document into the output document using specified input output file names and its extensions. |
|[ convert(input_file, output_file, save_format)](./convert/#str_str_saveformat) | Converts the given input document into the output document using specified input output file names and the final document format. |
|[ convert(input_file, output_file, save_options)](./convert/#str_str_saveoptions) | Converts the given input document into the output document using specified input output file names and save options. |
|[ convert(input_file, load_options, output_file, save_options)](./convert/#str_loadoptions_str_saveoptions) | Converts the given input document into the output document using specified input output file names its load/save options. |
|[ convert(input_stream, output_stream, save_format)](./convert/#bytesio_bytesio_saveformat) | Converts the given input document into a single output document using specified input and output streams. |
|[ convert(input_stream, output_stream, save_options)](./convert/#bytesio_bytesio_saveoptions) | Converts the given input document into a single output document using specified input and output streams. |
|[ convert(input_stream, load_options, output_stream, save_options)](./convert/#bytesio_loadoptions_bytesio_saveoptions) | Converts the given input document into a single output document using specified input and output streams. |
|[ convert_to_images(input_file, output_file)](./convert_to_images/#str_str) | Converts the pages of the specified input file to image files. |
|[ convert_to_images(input_file, output_file, save_format)](./convert_to_images/#str_str_saveformat) | Converts the pages of the specified input file to image files in the specified format. |
|[ convert_to_images(input_file, output_file, save_options)](./convert_to_images/#str_str_imagesaveoptions) | Converts the pages of the specified input file to image files using the specified save options. |
|[ convert_to_images(input_file, load_options, output_file, save_options)](./convert_to_images/#str_loadoptions_str_imagesaveoptions) | Converts the pages of the specified input file to image files using the provided load and save options. |
|[ convert_to_images(input_file, save_format)](./convert_to_images/#str_saveformat) | Converts the pages of the specified input file to images in the specified format and returns an array of streams containing the images. |
|[ convert_to_images(input_file, save_options)](./convert_to_images/#str_imagesaveoptions) | Converts the pages of the specified input file to images using the specified save options and returns an array of streams containing the images. |
|[ convert_to_images(input_stream, save_format)](./convert_to_images/#bytesio_saveformat) | Converts the pages of the specified input stream to images in the specified format and returns an array of streams containing the images. |
|[ convert_to_images(input_stream, save_options)](./convert_to_images/#bytesio_imagesaveoptions) | Converts the pages of the specified input stream to images using the specified save options and returns an array of streams containing the images. |
|[ convert_to_images(input_stream, load_options, save_options)](./convert_to_images/#bytesio_loadoptions_imagesaveoptions) | Converts the pages of the specified input stream to images using the provided load and save options, and returns an array of streams containing the images. |
|[ convert_to_images(doc, save_format)](./convert_to_images/#document_saveformat) | Converts the pages of the specified document to images in the specified format and returns an array of streams containing the images. |
|[ convert_to_images(doc, save_options)](./convert_to_images/#document_imagesaveoptions) | Converts the pages of the specified document to images using the specified save options and returns an array of streams containing the images. |
|[ create()](./create/#default) | Creates new instance of the converter processor. |
|[ create(context)](./create/#convertercontext) | Creates new instance of the converter processor. |
|[ execute()](../processor/execute/#default) | Execute the processor action.<br>(Inherited from [Processor](../processor/)) |
|[ from_file(input)](../processor/from_file/#str) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_file(input, load_options)](../processor/from_file/#str_loadoptions) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_stream(input)](../processor/from_stream/#bytesio) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_stream(input, load_options)](../processor/from_stream/#bytesio_loadoptions) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ to_file(output)](../processor/to_file/#str) | Specifies output file for the processor.<br>(Inherited from [Processor](../processor/)) |
|[ to_file(output, save_options)](../processor/to_file/#str_saveoptions) | Specifies output file for the processor.<br>(Inherited from [Processor](../processor/)) |
|[ to_file(output, save_format)](../processor/to_file/#str_saveformat) | Specifies output file for the processor.<br>(Inherited from [Processor](../processor/)) |
|[ to_stream(output, save_options)](../processor/to_stream/#bytesio_saveoptions) | Specifies output stream for the processor.<br>(Inherited from [Processor](../processor/)) |
|[ to_stream(output, save_format)](../processor/to_stream/#bytesio_saveformat) | Specifies output stream for the processor.<br>(Inherited from [Processor](../processor/)) |
|[ to_streams(output, save_options)](../processor/to_streams/#unknown_saveoptions) | <br>(Inherited from [Processor](../processor/)) |
|[ to_streams(output, save_format)](../processor/to_streams/#unknown_saveformat) | <br>(Inherited from [Processor](../processor/)) |

### See Also

* module [aspose.words.lowcode](../)
* class [Processor](../processor/)

