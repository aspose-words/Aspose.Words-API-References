---
title: Merger class
linktitle: Merger class
articleTitle: Merger class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Merger class. Represents a group of methods intended to merge a variety of different types of documents into a single output document."
type: docs
weight: 100
url: /python-net/aspose.words.lowcode/merger/
---

## Merger class

Represents a group of methods intended to merge a variety of different types of documents into a single output document.


### Remarks

The specified input and output files or streams, along with the desired merge and save options,
are used to merge the given input documents into a single output document.

The merging functionality supports over 35 different file formats.




**Inheritance:** [Merger](./) → [Processor](../processor/)

### Methods

| Name | Description |
| --- | --- |
|[ create()](./create/#default) | Creates new instance of the mail merger processor. |
|[ create(context)](./create/#mergercontext) | Creates new instance of the mail merger processor. |
|[ execute()](../processor/execute/#default) | Execute the processor action.<br>(Inherited from [Processor](../processor/)) |
|[ from_file(input)](../processor/from_file/#str) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_file(input, load_options)](../processor/from_file/#str_loadoptions) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_stream(input)](../processor/from_stream/#bytesio) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_stream(input, load_options)](../processor/from_stream/#bytesio_loadoptions) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ merge(output_file, input_files)](./merge/#str_strlist) | Merges the given input documents into a single output document using specified input and output file names using [MergeFormatMode.KEEP_SOURCE_FORMATTING](../mergeformatmode/#KEEP_SOURCE_FORMATTING). |
|[ merge(output_file, input_files, save_format, merge_format_mode)](./merge/#str_strlist_saveformat_mergeformatmode) | Merges the given input documents into a single output document using specified input output file names and the final document format. |
|[ merge(output_file, input_files, save_options, merge_format_mode)](./merge/#str_strlist_saveoptions_mergeformatmode) | Merges the given input documents into a single output document using specified input output file names and save options. |
|[ merge(output_file, input_files, load_options, save_options, merge_format_mode)](./merge/#str_strlist_loadoptionslist_saveoptions_mergeformatmode) | Merges the given input documents into a single output document using specified input output file names and save options. |
|[ merge(input_files, merge_format_mode)](./merge/#strlist_mergeformatmode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
|[ merge(input_files, load_options, merge_format_mode)](./merge/#strlist_loadoptionslist_mergeformatmode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
|[ merge_docs(input_documents, merge_format_mode)](./merge_docs/#documentlist_mergeformatmode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
|[ merge_streams(output_stream, input_streams, save_format)](./merge_streams/#bytesio_bytesiolist_saveformat) | Merges the given input documents into a single output document using specified input output streams and the final document format. |
|[ merge_streams(output_stream, input_streams, save_options, merge_format_mode)](./merge_streams/#bytesio_bytesiolist_saveoptions_mergeformatmode) | Merges the given input documents into a single output document using specified input output streams and save options. |
|[ merge_streams(output_stream, input_streams, load_options, save_options, merge_format_mode)](./merge_streams/#bytesio_bytesiolist_loadoptionslist_saveoptions_mergeformatmode) | Merges the given input documents into a single output document using specified input output streams and save options. |
|[ merge_streams(input_streams, merge_format_mode)](./merge_streams/#bytesiolist_mergeformatmode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
|[ merge_streams(input_streams, load_options, merge_format_mode)](./merge_streams/#bytesiolist_loadoptionslist_mergeformatmode) | Merges the given input documents into a single document and returns [Document](../../aspose.words/document/) instance of the final document. |
|[ merge_to_images(input_files, save_options, merge_format_mode)](./merge_to_images/#strlist_imagesaveoptions_mergeformatmode) | Merges the given input documents into a single output document using specified input output file names and save options. Renders the output to images. |
|[ merge_to_images_streams(input_streams, save_options, merge_format_mode)](./merge_to_images_streams/#bytesiolist_imagesaveoptions_mergeformatmode) | Merges the given input document streams into a single output document using specified image save options. Renders the output to images. |
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

