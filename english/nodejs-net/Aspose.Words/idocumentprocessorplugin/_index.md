---
title: IDocumentProcessorPlugin class
linktitle: IDocumentProcessorPlugin class
articleTitle: IDocumentProcessorPlugin class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.IDocumentProcessorPlugin class. Defines an interface for external document processor plugin."
type: docs
weight: 550
url: /nodejs-net/aspose.words/idocumentprocessorplugin/
---

## IDocumentProcessorPlugin class

Defines an interface for external document processor plugin.


### Methods

| Name | Description |
| --- | --- |
|[ append(inputStream, loadOptions)](./append/#buffer_loadoptions) | Append the document loading it with the specified load options. |
|[ load(inputStream, loadOptions)](./load/#buffer_loadoptions) | Load the document using the specified load options. |
|[ save(outputStream, saveOptions)](./save/#buffer_saveoptions) | Save the document loaded by [IDocumentProcessorPlugin.load()](./load/#buffer_loadoptions) method to the output stream using the specified save options. |
|[ setImageWatermark(imageWatermark, imageWatermarkOptions)](./setImageWatermark/#buffer_imagewatermarkoptions) | Adds image watermark on each page of the document loaded by [IDocumentProcessorPlugin.load()](./load/#buffer_loadoptions) method. |
|[ setTextWatermark(textWatermark, textWatermarkOptions)](./setTextWatermark/#string_textwatermarkoptions) | Adds text watermark on each page of the document loaded by [IDocumentProcessorPlugin.load()](./load/#buffer_loadoptions) method. |
|[ toDocument()](./toDocument/#default) | Parses the document loaded by [IDocumentProcessorPlugin.load()](./load/#buffer_loadoptions) method into [Document](../document/) object. |
|[ toPages(saveOptions)](./toPages/#fixedpagesaveoptions) | Saves each page of the document loaded by [IDocumentProcessorPlugin.load()](./load/#buffer_loadoptions) method using the specified fixed page save options. |

### See Also

* module [Aspose.Words](../)

