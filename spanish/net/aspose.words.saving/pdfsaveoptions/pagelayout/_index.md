---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words para .NET
description: Descubre la propiedad PdfSaveOptions PageLayout para personalizar el diseño de tu PDF y optimizar su visualización en cualquier lector. ¡Mejora la presentación de tu documento!
type: docs
weight: 250
url: /es/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Especifica el diseño de página que se utilizará cuando el documento se abra en un lector de PDF.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Observaciones

El valor predeterminado esSinglePage .

## Ejemplos

Muestra cómo mostrar páginas cuando se abren en un lector de PDF.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Muestra las páginas de dos en dos, con las páginas impares a la izquierda.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Ver también

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
