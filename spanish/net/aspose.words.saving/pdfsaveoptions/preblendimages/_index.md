---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words para .NET
description: Descubra la propiedad PreblendImages de PdfSaveOptions. Controle fácilmente la fusión de imágenes transparentes para mejorar la calidad y el atractivo visual del documento.
type: docs
weight: 270
url: /es/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Obtiene o establece un valor que determina si se deben precombinar o no imágenes transparentes con color de fondo negro.

```csharp
public bool PreblendImages { get; set; }
```

## Observaciones

La precombinación de imágenes puede mejorar la apariencia visual del documento PDF en Adobe Reader y eliminar los artefactos de suavizado.

Para mostrar correctamente las imágenes premezcladas, la aplicación de visualización de PDF debe admitir la entrada /Matte en el diccionario de imágenes de máscara suave. Además, la premezcla de imágenes puede reducir el rendimiento de la representación de PDF.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo precombinar imágenes con fondos transparentes al guardar un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Establezca la propiedad "PreblendImages" en "true" para premezclar imágenes transparentes
// con un fondo, que puede reducir los artefactos.
// Establezca la propiedad "PreblendImages" en "falso" para representar imágenes transparentes normalmente.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
