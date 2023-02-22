---
title: PclSaveOptions.RasterizeTransformedElements
second_title: Referencia de API de Aspose.Words para .NET
description: PclSaveOptions propiedad. Obtiene o establece un valor que determina si los elementos transformados complejos se deben rasterizar o no antes de guardarlos en el documento PCL. El valor predeterminado esverdadero .
type: docs
weight: 30
url: /es/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Obtiene o establece un valor que determina si los elementos transformados complejos se deben rasterizar o no antes de guardarlos en el documento PCL. El valor predeterminado es`verdadero` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

### Observaciones

PCL no admite algunos tipos de transformaciones que utiliza Aspose Words. Por ejemplo, imágenes giradas y sesgadas y pinceles de textura. Para representar correctamente dichos elementos, se utiliza el proceso de rasterización , es decir, guardar en la imagen y recortar. Este proceso puede requerir tiempo y memoria adicionales. Si el indicador está configurado en`falso` parte del contenido de salida puede ser diferente en comparación con el documento de origen.

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


