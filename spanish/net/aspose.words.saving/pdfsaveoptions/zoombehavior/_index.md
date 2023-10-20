---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words para .NET
description: PdfSaveOptions ZoomBehavior propiedad. Obtiene o establece un valor que determina qué tipo de zoom se debe aplicar cuando se abre un documento con un visor de PDF en C#.
type: docs
weight: 320
url: /es/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Obtiene o establece un valor que determina qué tipo de zoom se debe aplicar cuando se abre un documento con un visor de PDF.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Observaciones

El valor predeterminado esNone , es decir, no se aplica ningún ajuste.

## Ejemplos

Muestra cómo configurar el zoom predeterminado que aplica un lector al abrir un documento PDF renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
// Establece la propiedad "ZoomBehavior" en "PdfZoomBehavior.ZoomFactor" para obtener un lector de PDF
// aplicamos un factor de zoom basado en porcentaje cuando abrimos el documento con él.
// Establece la propiedad "ZoomFactor" en "25" para darle al factor de zoom un valor del 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Cuando abrimos este documento usando un lector como Adobe Acrobat, veremos el documento escalado a 1/4 de su tamaño real.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Ver también

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
