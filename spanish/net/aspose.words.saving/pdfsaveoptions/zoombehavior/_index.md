---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words para .NET
description: Descubre PdfSaveOptions ZoomBehavior y controla la configuración de zoom para una visualización óptima en los visores de PDF. ¡Mejora la experiencia del usuario con una visualización personalizada de documentos!
type: docs
weight: 350
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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
