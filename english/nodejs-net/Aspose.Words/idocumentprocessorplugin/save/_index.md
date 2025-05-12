---
title: IDocumentProcessorPlugin.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Node.js
description: "IDocumentProcessorPlugin.save method. Save the document loaded by [IDocumentProcessorPlugin.load()](../load/#buffer_loadoptions) method to the output stream using the specified save options."
type: docs
weight: 30
url: /nodejs-net/aspose.words/idocumentprocessorplugin/save/
---

## save(outputStream, saveOptions) {#buffer_saveoptions}

Save the document loaded by [IDocumentProcessorPlugin.load()](../load/#buffer_loadoptions) method to the output stream using the specified save options.



```js
save(outputStream: Buffer, saveOptions: Aspose.Words.Saving.SaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | Buffer | The output stream. |
| saveOptions | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

### Remarks

If the specified output format is image, only the first page image is saved to the output stream.
If the specified save format is not natively supported by the plugin (requires loading to [Document](../../document/)),
method throws an exception.


### See Also

* module [Aspose.Words](../../)
* class [IDocumentProcessorPlugin](../)

