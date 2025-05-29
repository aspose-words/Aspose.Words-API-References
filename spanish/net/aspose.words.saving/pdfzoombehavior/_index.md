---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.PdfZoomBehavior para personalizar la configuración de zoom de PDF. Mejore la experiencia del usuario con opciones de visualización personalizadas en documentos PDF.
type: docs
weight: 6340
url: /es/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Especifica el tipo de zoom que se aplica a un documento PDF cuando se abre en un visor de PDF.

```csharp
public enum PdfZoomBehavior
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | La visualización del documento queda a criterio del visor de PDF. Normalmente, el visor muestra el documento a la medida del ancho de la página. |
| ZoomFactor | `1` | Muestra la página utilizando el factor de zoom especificado. |
| FitPage | `2` | Muestra la página para que sea visible en su totalidad. |
| FitWidth | `3` | Se ajusta al ancho de la página. |
| FitHeight | `4` | Se ajusta a la altura de la página. |
| FitBox | `5` | Se ajusta al cuadro delimitador (rectángulo que contiene todos los elementos visibles en la página). |

## Ejemplos

Muestra cómo configurar el zoom predeterminado que aplica un lector al abrir un documento PDF renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
// Establezca la propiedad "ZoomBehavior" en "PdfZoomBehavior.ZoomFactor" para que un lector de PDF
// aplicamos un factor de zoom basado en porcentaje cuando abrimos el documento con él.
// Establezca la propiedad "ZoomFactor" en "25" para darle al factor de zoom un valor del 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Cuando abramos este documento utilizando un lector como Adobe Acrobat, veremos el documento escalado a 1/4 de su tamaño real.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
