---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words para .NET
description: Controle la rasterización de elementos complejos en documentos PCL con PclSaveOptions. Gestione fácilmente la calidad de la imagen y el tamaño del archivo para obtener resultados óptimos.
type: docs
weight: 30
url: /es/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Obtiene o establece un valor que determina si los elementos transformados complejos deben rasterizarse o no antes de guardarlos en el documento PCL. El valor predeterminado es`verdadero` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Observaciones

PCL no admite algunos tipos de transformaciones utilizadas por Aspose Words. Por ejemplo, imágenes rotadas o sesgadas y pinceles de textura. Para renderizar correctamente estos elementos, se utiliza un proceso de rasterización, es decir, guardar en la imagen y recortar. Este proceso puede requerir tiempo y memoria adicionales. Si el indicador está configurado en`FALSO` , algunos contenidos en la salida pueden ser diferentes en comparación con el documento de origen.

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

* class [PclSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
