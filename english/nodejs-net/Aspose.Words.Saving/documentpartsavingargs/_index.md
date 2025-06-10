---
title: DocumentPartSavingArgs class
linktitle: DocumentPartSavingArgs class
articleTitle: DocumentPartSavingArgs class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.DocumentPartSavingArgs class. Provides data for the [IDocumentPartSavingCallback.documentPartSaving()](../idocumentpartsavingcallback/documentPartSaving/#documentpartsavingargs) callback"
type: docs
weight: 110
url: /nodejs-net/aspose.words.saving/documentpartsavingargs/
---

## DocumentPartSavingArgs class

Provides data for the [IDocumentPartSavingCallback.documentPartSaving()](../idocumentpartsavingcallback/documentPartSaving/#documentpartsavingargs) callback.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Remarks

When Aspose.Words saves a document to HTML or related formats and [HtmlSaveOptions.documentSplitCriteria](../htmlsaveoptions/documentSplitCriteria/) 
is specified, the document is split into parts and by default, each document part is saved into a separate file.

Class [DocumentPartSavingArgs](./) allows you to control how each document part will be saved. 
It allows to redefine how file names are generated or to completely circumvent saving of document parts into 
files by providing your own stream objects.

To save document parts into streams instead of files, use the Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream property.




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the document object that is being saved. |
| [documentPartFileName](./documentPartFileName/) | Gets or sets the file name (without path) where the document part will be saved to. |
| [keepDocumentPartStreamOpen](./keepDocumentPartStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document part. |

### See Also

* module [Aspose.Words.Saving](../)

