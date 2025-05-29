---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words para .NET
description: Guarde documentos sin esfuerzo con el método de guardado IDocumentProcessorPlugin, garantizando un resultado óptimo con opciones de guardado personalizables para sus necesidades.
type: docs
weight: 30
url: /es/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Guardar el documento cargado por[`Load`](../load/) método para el flujo de salida utilizando las opciones de guardado especificadas.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| outputStream | Stream | El flujo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |

## Observaciones

Si el formato de salida especificado es imagen, solo se guarda la imagen de la primera página en el flujo de salida. Si el complemento no admite de forma nativa el formato de guardado especificado (requiere carga en el servidor)[`Document`](../../document/)), el método lanza una excepción.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
