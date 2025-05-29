---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words para .NET
description: Descubra la propiedad InterpolateImages de PdfSaveOptions, una función clave que mejora la calidad de imagen de sus documentos. ¡Optimice sus PDF sin esfuerzo!
type: docs
weight: 210
url: /es/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Una bandera que indica si la interpolación de imágenes debe ser realizada por un lector conforme. Cuando`FALSO` Si se especifica, la bandera no se escribe en el documento de salida y en su lugar se utiliza el comportamiento predeterminado del lector.

```csharp
public bool InterpolateImages { get; set; }
```

## Observaciones

Cuando la resolución de una imagen de origen es significativamente menor que la del dispositivo de salida, cada muestra de origen cubre muchos píxeles del dispositivo. Como resultado, las imágenes pueden aparecer irregulares o con forma de bloques. Estos artefactos visuales se pueden reducir aplicando un algoritmo de interpolación de imágenes durante el renderizado. En lugar de pintar todos los píxeles cubiertos por una muestra de origen con el mismo color, la interpolación de imágenes intenta producir una transición suave entre los valores de muestra adyacentes.

Un lector conforme puede elegir no implementar esta función de PDF, o puede usar cualquier implementación específica de interpolación que desee.

El valor predeterminado es`FALSO`.

La bandera de interpolación está prohibida por la conformidad con PDF/A.`FALSO` El valor se utilizará automáticamente al guardar en PDF/A.

## Ejemplos

Muestra cómo realizar interpolación en imágenes al guardar un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Establezca la propiedad "InterpolateImages" en "true" para que el lector que abra este documento interpole imágenes.
//Su resolución debe ser menor que la del dispositivo que muestra el documento.
// Establezca la propiedad "InterpolateImages" en "false" para que el lector no aplique ninguna interpolación.
saveOptions.InterpolateImages = interpolateImages;

// Cuando abramos este documento con un lector como Adobe Acrobat, necesitaremos hacer zoom en la imagen
// para ver el efecto de interpolación si guardamos el documento con ella habilitada.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
