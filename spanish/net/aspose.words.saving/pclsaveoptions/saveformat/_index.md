---
title: PclSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveFormat de PclSaveOptions para guardar fácilmente documentos en formato PCL, garantizando compatibilidad y resultados de alta calidad para sus proyectos.
type: docs
weight: 40
url: /es/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedePcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Ejemplos

Muestra cómo rasterizar elementos complejos al guardar un documento en PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
