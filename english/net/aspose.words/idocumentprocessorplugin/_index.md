---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words IDocumentProcessorPlugin interface to enhance your document processing with powerful external plugins for seamless integration.
type: docs
weight: 3630
url: /net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Defines an interface for external document processor plugin.

```csharp
public interface IDocumentProcessorPlugin
```

## Methods

| Name | Description |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Append the document loading it with the specified load options. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Load the document using the specified load options. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Save the document loaded by [`Load`](./load/) method to the output stream using the specified save options. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Adds image watermark on each page of the document loaded by [`Load`](./load/) method. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Adds text watermark on each page of the document loaded by [`Load`](./load/) method. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | Parses the document loaded by [`Load`](./load/) method into [`Document`](../document/) object. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Saves each page of the document loaded by [`Load`](./load/) method using the specified fixed page save options. |

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
