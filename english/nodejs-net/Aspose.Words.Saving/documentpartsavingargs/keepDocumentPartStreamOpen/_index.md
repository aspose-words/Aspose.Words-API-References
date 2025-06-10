---
title: DocumentPartSavingArgs.keepDocumentPartStreamOpen property
linktitle: keepDocumentPartStreamOpen property
articleTitle: keepDocumentPartStreamOpen property
second_title: Aspose.Words for Node.js
description: "DocumentPartSavingArgs.keepDocumentPartStreamOpen property. Specifies whether Aspose.Words should keep the stream open or close it after saving a document part."
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/documentpartsavingargs/keepDocumentPartStreamOpen/
---

## DocumentPartSavingArgs.keepDocumentPartStreamOpen property

Specifies whether Aspose.Words should keep the stream open or close it after saving a document part.


```js
get keepDocumentPartStreamOpen(): boolean
```

### Remarks

Default is ``false`` and Aspose.Words will close the stream you provided
in the Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream property after writing a document part into it.
Specify ``true`` to keep the stream open. Please note that the main output stream 
provided in the call to Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat) or 
Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions) will never be closed by Aspose.Words 
even if [DocumentPartSavingArgs.keepDocumentPartStreamOpen](./) is set to ``false``.




### See Also

* module [Aspose.Words.Saving](../../)
* class [DocumentPartSavingArgs](../)

