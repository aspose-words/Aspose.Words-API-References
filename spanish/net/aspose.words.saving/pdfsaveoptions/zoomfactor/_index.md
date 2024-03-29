---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words para .NET
description: PdfSaveOptions ZoomFactor propiedad. Obtiene o establece un valor que determina el factor de zoom en porcentajes para un documento en C#.
type: docs
weight: 330
url: /es/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Obtiene o establece un valor que determina el factor de zoom (en porcentajes) para un documento.

```csharp
public int ZoomFactor { get; set; }
```

## Observaciones

Este valor se utiliza sólo si[`ZoomBehavior`](../zoombehavior/) se establece enZoomFactor .

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

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
