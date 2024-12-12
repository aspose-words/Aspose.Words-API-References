---
title: Splitter class
linktitle: Splitter class
articleTitle: Splitter class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Splitter class. Provides methods intended to split the documents into parts using different criteria."
type: docs
weight: 80
url: /python-net/aspose.words.lowcode/splitter/
---

## Splitter class

Provides methods intended to split the documents into parts using different criteria.


### Methods

| Name | Description |
| --- | --- |
|[ extract_pages(input_file_name, output_file_name, start_page_index, page_count)](./extract_pages/#str_str_int_int) | Extracts a specified range of pages from a document file and saves the extracted pages  to a new file. The output file format is determined by the extension of the output file name. |
|[ extract_pages(input_file_name, output_file_name, save_format, start_page_index, page_count)](./extract_pages/#str_str_saveformat_int_int) | Extracts a specified range of pages from a document file and saves the extracted pages  to a new file using the specified save format. |
|[ extract_pages(input_stream, output_stream, save_format, start_page_index, page_count)](./extract_pages/#bytesio_bytesio_saveformat_int_int) | Extracts a specified range of pages from a document stream and saves the extracted pages  to an output stream using the specified save format. |
|[ remove_blank_pages(input_file_name, output_file_name)](./remove_blank_pages/#str_str) | Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed. |
|[ remove_blank_pages(input_file_name, output_file_name, save_format)](./remove_blank_pages/#str_str_saveformat) | Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed. |
|[ remove_blank_pages(input_stream, output_stream, save_format)](./remove_blank_pages/#bytesio_bytesio_saveformat) | Removes blank pages from a document provided in an input stream and saves the updated document  to an output stream in the specified save format. Returns a list of page numbers that were removed. |
|[ split(input_file_name, output_file_name, options)](./split/#str_str_splitoptions) | Splits a document into multiple parts based on the specified split options and saves  the resulting parts to files. The output file format is determined by the extension of the output file name. |
|[ split(input_file_name, output_file_name, save_format, options)](./split/#str_str_saveformat_splitoptions) | Splits a document into multiple parts based on the specified split options and saves  the resulting parts to files in the specified save format. |
|[ split(input_stream, save_format, options)](./split/#bytesio_saveformat_splitoptions) | Splits a document from an input stream into multiple parts based on the specified split options and  returns the resulting parts as an array of streams in the specified save format. |

### See Also

* module [aspose.words.lowcode](../)

