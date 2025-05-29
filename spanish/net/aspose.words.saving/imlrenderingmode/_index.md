---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words ImlRenderingMode para una representación óptima de InkML. ¡Mejore la producción de sus documentos con una visualización precisa de objetos de tinta!
type: docs
weight: 6000
url: /es/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Especifica cómo se representan los objetos de tinta (InkML) en formatos de página fijos.

```csharp
public enum ImlRenderingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Fallback | `0` | Si la forma de respaldo está disponible para el objeto de tinta (InkML), Aspose.Words representa la forma de respaldo en lugar de InkML. |
| InkML | `1` | Aspose.Words ignora la forma de reserva del objeto de tinta (InkML) y renderiza InkML en sí. Este es el modo predeterminado. |

## Ejemplos

Muestra cómo renderizar el objeto Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Establecer 'ImlRenderingMode.InkML' ignora la forma de reserva del objeto de tinta (InkML) y representa InkML en sí.
// Si el resultado de la representación no es satisfactorio,
// utilice 'ImlRenderingMode.Fallback' para obtener un resultado similar a las versiones anteriores.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
