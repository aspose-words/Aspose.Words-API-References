---
title: document_part_stream property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify the stream where the document part will be saved to."
type: docs
weight: 30
url: /python-net/aspose.words.saving/documentpartsavingargs/document_part_stream/
---

## DocumentPartSavingArgs.document_part_stream property

Allows to specify the stream where the document part will be saved to.

This property allows you to save document parts to streams instead of files during HTML export.

The default value is ``None``. When this property is ``None``, the document part 
will be saved to a file specified in the [DocumentPartSavingArgs.document_part_file_name](../document_part_file_name/) property.

When saving to a stream in HTML format is requested by [Document.save()](../../../aspose.words/document/save/#bytesio_saveformat) 
or [Document.save()](../../../aspose.words/document/save/#bytesio_saveoptions) and first document part is about to be saved, 
Aspose.Words suggests here the main output stream initially passed by the caller.

When saving to EPUB format that is a container format based on HTML, [DocumentPartSavingArgs.document_part_stream](./) cannot 
be specified because all subsidiary parts will be encapsulated into a single output package.




### See Also

* module [aspose.words.saving](../../)
* class [DocumentPartSavingArgs](../)
* property [DocumentPartSavingArgs.keep_document_part_stream_open](../keep_document_part_stream_open/)

