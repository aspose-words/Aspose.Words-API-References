---
title: IDocumentProcessorPlugin.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "IDocumentProcessorPlugin.save method. Save the document loaded by [IDocumentProcessorPlugin.load()](../load/#bytesio_loadoptions) method to the output stream using the specified save options."
type: docs
weight: 30
url: /python-net/aspose.words/idocumentprocessorplugin/save/
---

## save(output_stream, save_options) {#bytesio_saveoptions}

Save the document loaded by [IDocumentProcessorPlugin.load()](../load/#bytesio_loadoptions) method to the output stream using the specified save options.



```python
def save(self, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

### Remarks

If the specified output format is image, only the first page image is saved to the output stream.
If the specified save format is not natively supported by the plugin (requires loading to [Document](../../document/)),
method throws an exception.


### See Also

* module [aspose.words](../../)
* class [IDocumentProcessorPlugin](../)

