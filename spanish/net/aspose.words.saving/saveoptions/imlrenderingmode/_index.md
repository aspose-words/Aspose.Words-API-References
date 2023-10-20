---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words para .NET
description: SaveOptions ImlRenderingMode propiedad. Obtiene o establece un valor que determina cómo se representan los objetos de tinta InkML en C#.
type: docs
weight: 90
url: /es/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML).

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Observaciones

El valor predeterminado esInkML .

Esta propiedad se utiliza cuando el documento se exporta a formatos de página fijos.

## Ejemplos

Muestra cómo renderizar el objeto Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Establecer 'ImlRenderingMode.InkML' ignora la forma alternativa del objeto de tinta (InkML) y representa el propio InkML.
// Si el resultado del renderizado no es satisfactorio,
// utilice 'ImlRenderingMode.Fallback' para obtener un resultado similar a las versiones anteriores.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Ver también

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
