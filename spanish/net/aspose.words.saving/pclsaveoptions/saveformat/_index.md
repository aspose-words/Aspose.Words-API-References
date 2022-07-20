---
title: SaveFormat
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedePcl .
type: docs
weight: 40
url: /es/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedePcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Ejemplos

Muestra cómo rasterizar elementos complejos mientras se guarda un documento en PCL.

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

* enum [SaveFormat](../../../aspose.words/saveformat)
* class [PclSaveOptions](../../pclsaveoptions)
* espacio de nombres [Aspose.Words.Saving](../../pclsaveoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->