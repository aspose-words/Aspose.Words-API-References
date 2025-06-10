---
title: CssSavingArgs class
linktitle: CssSavingArgs class
articleTitle: CssSavingArgs class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.CssSavingArgs class. Provides data for the [ICssSavingCallback.cssSaving()](../icsssavingcallback/cssSaving/#csssavingargs) event"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/csssavingargs/
---

## CssSavingArgs class

Provides data for the [ICssSavingCallback.cssSaving()](../icsssavingcallback/cssSaving/#csssavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Remarks

By default, when Aspose.Words saves a document to HTML, it saves CSS information inline
(as a value of the **style** attribute on every element).


[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

To save CSS into stream, use the Aspose.Words.Saving.CssSavingArgs.CssStream property.

To suppress saving CSS into a file and embedding to HTML document use the [CssSavingArgs.isExportNeeded](./isExportNeeded/) property.




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the document object that is currently being saved. |
| [isExportNeeded](./isExportNeeded/) | Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is ``true``. When this property is ``false``, the CSS information will not be saved to a CSS file and will not be embedded to HTML document. |
| [keepCssStreamOpen](./keepCssStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |

### See Also

* module [Aspose.Words.Saving](../)

