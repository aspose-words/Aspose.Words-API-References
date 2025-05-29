---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words para .NET
description: Descubra la interfaz Aspose.Words IDocumentProcessorPlugin para mejorar el procesamiento de sus documentos con potentes complementos externos para una integración perfecta.
type: docs
weight: 3610
url: /es/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Define una interfaz para el complemento de procesador de documentos externo.

```csharp
public interface IDocumentProcessorPlugin
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anexa el documento cargándolo con las opciones de carga especificadas. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Cargue el documento utilizando las opciones de carga especificadas. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Guardar el documento cargado por[`Load`](./load/) método para el flujo de salida utilizando las opciones de guardado especificadas. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Agrega una marca de agua de imagen en cada página del documento cargado por[`Load`](./load/) método. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Agrega una marca de agua de texto en cada página del documento cargado por[`Load`](./load/) método. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | Analiza el documento cargado por[`Load`](./load/) método en[`Document`](../document/) objeto. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Guarda cada página del documento cargado por[`Load`](./load/) método que utiliza las opciones de guardado de página fija especificadas. |

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
