---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words para .NET
description: Descubra la propiedad FixedPageSaveOptions ColorMode para personalizar la representación del color y mejorar la calidad y el atractivo visual del documento. ¡Optimice su producción hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Obtiene o establece un valor que determina cómo se representan los colores.

```csharp
public ColorMode ColorMode { get; set; }
```

## Observaciones

El valor predeterminado esNormal .

## Ejemplos

Muestra cómo cambiar el color de la imagen con la propiedad de opciones de guardado.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
// Establezca la propiedad "ColorMode" en "Escala de grises" para representar todas las imágenes del documento en blanco y negro.
//El tamaño del documento de salida puede ser mayor con esta configuración.
// Establezca la propiedad "ColorMode" en "Normal" para representar todas las imágenes en color.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Ver también

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
