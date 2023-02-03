---
title: DocumentPartSavingArgs class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides data for the [IDocumentPartSavingCallback.document_part_saving()](../idocumentpartsavingcallback/document_part_saving/#documentpartsavingargs) callback"
type: docs
weight: 100
url: /python-net/aspose.words.saving/documentpartsavingargs/
---

## DocumentPartSavingArgs class

Provides data for the [IDocumentPartSavingCallback.document_part_saving()](../idocumentpartsavingcallback/document_part_saving/#documentpartsavingargs) callback.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




When Aspose.Words saves a document to HTML or related formats and [HtmlSaveOptions.document_split_criteria](../htmlsaveoptions/document_split_criteria/) 
is specified, the document is split into parts and by default, each document part is saved into a separate file.

Class [DocumentPartSavingArgs](./) allows you to control how each document part will be saved. 
It allows to redefine how file names are generated or to completely circumvent saving of document parts into 
files by providing your own stream objects.

To save document parts into streams instead of files, use the [DocumentPartSavingArgs.document_part_stream](./document_part_stream/) property.




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the document object that is being saved. |
| [document_part_file_name](./document_part_file_name/) | Gets or sets the file name (without path) where the document part will be saved to. |
| [document_part_stream](./document_part_stream/) | Allows to specify the stream where the document part will be saved to. |
| [keep_document_part_stream_open](./keep_document_part_stream_open/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document part. |

### See Also

* module [aspose.words.saving](../)

