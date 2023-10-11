---
title: PclSaveOptions.RasterizeTransformedElements
second_title: Referencia de API de Aspose.Words para .NET
description: PclSaveOptions propiedad. Obtiene o establece un valor que determina si los elementos transformados complejos deben rasterizarse o no antes de guardarlos en un documento PCL. El valor predeterminado esverdadero .
type: docs
weight: 30
url: /es/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Obtiene o establece un valor que determina si los elementos transformados complejos deben rasterizarse o no antes de guardarlos en un documento PCL. El valor predeterminado es`verdadero` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

### Observaciones

PCL no admite algunos tipos de transformaciones que utiliza Aspose Words. Por ejemplo, imágenes rotadas, sesgadas y pinceles de textura. Para renderizar adecuadamente dichos elementos se utiliza el proceso de rasterización, es decir, guardar en imagen y recortar. Este proceso puede consumir tiempo y memoria adicionales. Si el indicador está configurado en`FALSO` , parte del contenido de la salida puede ser diferente en comparación con el documento fuente.

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

* class [PclSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pclsaveoptions/)
* asamblea [Aspose.Words](../../../)


