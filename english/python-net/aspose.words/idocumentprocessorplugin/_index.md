---
title: IDocumentProcessorPlugin class
linktitle: IDocumentProcessorPlugin class
articleTitle: IDocumentProcessorPlugin class
second_title: Aspose.Words for Python
description: "aspose.words.IDocumentProcessorPlugin class. Defines an interface for external document processor plugin."
type: docs
weight: 550
url: /python-net/aspose.words/idocumentprocessorplugin/
---

## IDocumentProcessorPlugin class

Defines an interface for external document processor plugin.


### Methods

| Name | Description |
| --- | --- |
|[ append(input_stream, load_options)](./append/#bytesio_loadoptions) | Append the document loading it with the specified load options. |
|[ load(input_stream, load_options)](./load/#bytesio_loadoptions) | Load the document using the specified load options. |
|[ save(output_stream, save_options)](./save/#bytesio_saveoptions) | Save the document loaded by [IDocumentProcessorPlugin.load()](./load/#bytesio_loadoptions) method to the output stream using the specified save options. |
|[ set_image_watermark(image_watermark, image_watermark_options)](./set_image_watermark/#bytesio_imagewatermarkoptions) | Adds image watermark on each page of the document loaded by [IDocumentProcessorPlugin.load()](./load/#bytesio_loadoptions) method. |
|[ set_text_watermark(text_watermark, text_watermark_options)](./set_text_watermark/#str_textwatermarkoptions) | Adds text watermark on each page of the document loaded by [IDocumentProcessorPlugin.load()](./load/#bytesio_loadoptions) method. |
|[ to_document()](./to_document/#default) | Parses the document loaded by [IDocumentProcessorPlugin.load()](./load/#bytesio_loadoptions) method into [Document](../document/) object. |
|[ to_pages(save_options)](./to_pages/#fixedpagesaveoptions) | Saves each page of the document loaded by [IDocumentProcessorPlugin.load()](./load/#bytesio_loadoptions) method using the specified fixed page save options. |

### See Also

* module [aspose.words](../)

