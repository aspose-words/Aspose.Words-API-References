---
title: Splitter class
linktitle: Splitter class
articleTitle: Splitter class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Splitter class. Provides methods intended to split the documents into parts using different criteria."
type: docs
weight: 220
url: /python-net/aspose.words.lowcode/splitter/
---

## Splitter class

Provides methods intended to split the documents into parts using different criteria.


**Inheritance:** [Splitter](./) → [Processor](../processor/)

### Methods

| Name | Description |
| --- | --- |
|[ create(context)](./create/#splittercontext) | Creates new instance of the splitter processor. |
|[ execute()](../processor/execute/#default) | Execute the processor action.<br>(Inherited from [Processor](../processor/)) |
|[ extract_pages(input_file_name, output_file_name, start_page_index, page_count)](./extract_pages/#str_str_int_int) | Extracts a specified range of pages from a document file and saves the extracted pages  to a new file. The output file format is determined by the extension of the output file name. |
|[ extract_pages(input_file_name, output_file_name, save_format, start_page_index, page_count)](./extract_pages/#str_str_saveformat_int_int) | Extracts a specified range of pages from a document file and saves the extracted pages  to a new file using the specified save format. |
|[ extract_pages(input_file_name, output_file_name, save_options, start_page_index, page_count)](./extract_pages/#str_str_saveoptions_int_int) | Extracts a specified range of pages from a document file and saves the extracted pages  to a new file using the specified save format. |
|[ extract_pages(input_stream, output_stream, save_format, start_page_index, page_count)](./extract_pages/#bytesio_bytesio_saveformat_int_int) | Extracts a specified range of pages from a document stream and saves the extracted pages  to an output stream using the specified save format. |
|[ extract_pages(input_stream, output_stream, save_options, start_page_index, page_count)](./extract_pages/#bytesio_bytesio_saveoptions_int_int) | Extracts a specified range of pages from a document stream and saves the extracted pages  to an output stream using the specified save format. |
|[ from_file(input)](../processor/from_file/#str) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_file(input, load_options)](../processor/from_file/#str_loadoptions) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_stream(input)](../processor/from_stream/#bytesio) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ from_stream(input, load_options)](../processor/from_stream/#bytesio_loadoptions) | Specifies input document for processing.<br>(Inherited from [Processor](../processor/)) |
|[ remove_blank_pages(input_file_name, output_file_name)](./remove_blank_pages/#str_str) | Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed. |
|[ remove_blank_pages(input_file_name, output_file_name, save_format)](./remove_blank_pages/#str_str_saveformat) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
|[ remove_blank_pages(input_file_name, output_file_name, save_options)](./remove_blank_pages/#str_str_saveoptions) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
|[ remove_blank_pages(input_stream, output_stream, save_format)](./remove_blank_pages/#bytesio_bytesio_saveformat) | Removes blank pages from a document provided in an input stream and saves the updated document  to an output stream in the specified save format. Returns a list of page numbers that were removed. |
|[ remove_blank_pages(input_stream, output_stream, save_options)](./remove_blank_pages/#bytesio_bytesio_saveoptions) | Removes blank pages from a document provided in an input stream and saves the updated document  to an output stream in the specified save format. Returns a list of page numbers that were removed. |
|[ split(input_file_name, output_file_name, options)](./split/#str_str_splitoptions) | Splits a document into multiple parts based on the specified split options and saves  the resulting parts to files. The output file format is determined by the extension of the output file name. |
|[ split(input_file_name, output_file_name, save_format, options)](./split/#str_str_saveformat_splitoptions) | Splits a document into multiple parts based on the specified split options and saves  the resulting parts to files in the specified save format. |
|[ split(input_file_name, output_file_name, save_options, options)](./split/#str_str_saveoptions_splitoptions) | Splits a document into multiple parts based on the specified split options and saves  the resulting parts to files in the specified save format. |
|[ split(input_stream, save_format, options)](./split/#bytesio_saveformat_splitoptions) | Splits a document from an input stream into multiple parts based on the specified split options and  returns the resulting parts as an array of streams in the specified save format. |
|[ split(input_stream, save_options, options)](./split/#bytesio_saveoptions_splitoptions) | Splits a document from an input stream into multiple parts based on the specified split options and  returns the resulting parts as an array of streams in the specified save format. |
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

