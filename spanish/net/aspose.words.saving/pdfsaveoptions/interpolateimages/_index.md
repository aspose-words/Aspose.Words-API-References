---
title: PdfSaveOptions.InterpolateImages
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Un indicador que indica si la interpolación de imágenes debe ser realizada por un lector conforme. CuandoFALSO se especifica la bandera no se escribe en el documento de salida y se utiliza en su lugar el comportamiento predeterminado del lector.
type: docs
weight: 210
url: /es/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Un indicador que indica si la interpolación de imágenes debe ser realizada por un lector conforme. Cuando`FALSO` se especifica, la bandera no se escribe en el documento de salida y se utiliza en su lugar el comportamiento predeterminado del lector.

```csharp
public bool InterpolateImages { get; set; }
```

### Observaciones

Cuando la resolución de una imagen de origen es significativamente menor que la del dispositivo de salida, cada muestra de origen cubre muchos píxeles del dispositivo. Como resultado, las imágenes pueden aparecer irregulares o en bloques. Estos artefactos visuales se pueden reducir aplicando un algoritmo de interpolación de imágenes durante la renderización. En lugar de pintar todos los píxeles cubiertos por una muestra de origen con el mismo color, image interpolation intenta producir una imagen suave. transición entre valores de muestra adyacentes.

Un lector conforme puede optar por no implementar esta característica de PDF, o puede utilizar cualquier implementación específica de interpolación que desee.

El valor predeterminado es`FALSO`.

El indicador de interpolación está prohibido por el cumplimiento de PDF/A.`FALSO` El valor se utilizará automáticamente al guardar en PDF/A.

### Ejemplos

Muestra cómo realizar interpolación en imágenes mientras se guarda un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establece la propiedad "InterpolateImages" en "true" para que el lector que abre este documento interpole imágenes.
// Su resolución debe ser inferior a la del dispositivo que muestra el documento.
// Establece la propiedad "InterpolateImages" en "false" para que el lector no aplique ninguna interpolación.
saveOptions.InterpolateImages = interpolateImages;

// Cuando abrimos este documento con un lector como Adobe Acrobat, necesitaremos hacer zoom en la imagen
// para ver el efecto de interpolación si guardamos el documento con él habilitado.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

Muestra cómo mejorar la calidad de una imagen en los documentos renderizados (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establece la propiedad "InterpolateImages" en "true" para que el lector que abre este documento interpole imágenes.
// Su resolución debe ser inferior a la del dispositivo que muestra el documento.
// Establece la propiedad "InterpolateImages" en "false" para que el lector no aplique ninguna interpolación.
saveOptions.InterpolateImages = interpolateImages;

// Cuando abrimos este documento con un lector como Adobe Acrobat, necesitaremos hacer zoom en la imagen
// para ver el efecto de interpolación si guardamos el documento con él habilitado.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


