---
title: PdfSaveOptions.PreblendImages
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Obtiene o establece un valor que determina si se deben precombinar imágenes transparentes con color de fondo negro.
type: docs
weight: 260
url: /es/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Obtiene o establece un valor que determina si se deben precombinar imágenes transparentes con color de fondo negro.

```csharp
public bool PreblendImages { get; set; }
```

### Observaciones

La combinación previa de imágenes puede mejorar la apariencia visual del documento PDF en Adobe Reader y eliminar artefactos de suavizado.

Para mostrar correctamente las imágenes precombinadas, la aplicación de visualización de PDF debe admitir la entrada /Matte en el diccionario de imágenes de máscara suave. Además, la precombinación de imágenes puede disminuir el rendimiento de procesamiento de PDF.

El valor predeterminado es`FALSO`.

### Ejemplos

Muestra cómo precombinar imágenes con fondos transparentes mientras se guarda un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "PreblendImages" en "true" para precombinar imágenes transparentes
// con un fondo, que puede reducir los artefactos.
// Establece la propiedad "PreblendImages" en "false" para representar imágenes transparentes normalmente.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Muestra cómo precombinar imágenes con fondos transparentes (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "PreblendImages" en "true" para precombinar imágenes transparentes
// con un fondo, que puede reducir los artefactos.
// Establece la propiedad "PreblendImages" en "false" para representar imágenes transparentes normalmente.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


