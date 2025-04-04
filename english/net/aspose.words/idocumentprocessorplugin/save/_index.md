---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: Effortlessly save documents with the IDocumentProcessorPlugin Save method, ensuring optimal output with customizable save options for your needs.
type: docs
weight: 30
url: /net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Save the document loaded by [`Load`](../load/) method to the output stream using the specified save options.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | Stream | The output stream. |
| saveOptions | SaveOptions | The save options. |

## Remarks

If the specified output format is image, only the first page image is saved to the output stream. If the specified save format is not natively supported by the plugin (requires loading to [`Document`](../../document/)), method throws an exception.

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
