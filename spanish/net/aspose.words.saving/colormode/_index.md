---
title: Enum ColorMode
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.ColorMode enumeración. Especifica cómo se representan los colores.
type: docs
weight: 4600
url: /es/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Especifica cómo se representan los colores.

```csharp
public enum ColorMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | `0` | Representación con colores sin modificar. |
| Grayscale | `1` | Representación con colores en una gama de tonos grises desde el blanco hasta el negro. |

### Ejemplos

Muestra cómo cambiar el color de la imagen con la propiedad de opciones de guardado.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
// Establezca la propiedad "Modo de color" en "Escala de grises" para representar todas las imágenes del documento en blanco y negro.
// El tamaño del documento de salida puede ser mayor con esta configuración.
// Establezca la propiedad "ColorMode" en "Normal" para representar todas las imágenes en color.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


