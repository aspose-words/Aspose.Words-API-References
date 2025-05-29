---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words para .NET
description: Descubra la propiedad ZoomFactor de PdfSaveOptions para ajustar fácilmente los niveles de zoom del documento en porcentajes, mejorando su experiencia de visualización de PDF.
type: docs
weight: 360
url: /es/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Obtiene o establece un valor que determina el factor de zoom (en porcentajes) para un documento.

```csharp
public int ZoomFactor { get; set; }
```

## Observaciones

Este valor se utiliza solo si[`ZoomBehavior`](../zoombehavior/) está configurado paraZoomFactor .

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

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
