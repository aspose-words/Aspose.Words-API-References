---
title: DocumentPartSavingArgs.documentPartFileName property
linktitle: documentPartFileName property
articleTitle: documentPartFileName property
second_title: Aspose.Words for Node.js
description: "DocumentPartSavingArgs.documentPartFileName property. Gets or sets the file name (without path) where the document part will be saved to."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/documentpartsavingargs/documentPartFileName/
---

## DocumentPartSavingArgs.documentPartFileName property

Gets or sets the file name (without path) where the document part will be saved to.


```js
get documentPartFileName(): string
```

### Remarks

This property allows you to redefine how the document part file names are generated
during export to HTML or EPUB.

When the callback is invoked, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the document part into a 
different file. Note that the file name for each part must be unique.

[DocumentPartSavingArgs.documentPartFileName](./) must contain only the file name without the path. 
Aspose.Words determines the path for saving using the document file name. If output document 
file name was not specified, for instance when saving to a stream, this file name is used only 
for referencing document parts. The same is true when saving to EPUB format.




### See Also

* module [Aspose.Words.Saving](../../)
* class [DocumentPartSavingArgs](../)

