---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.PdfPageLayout para una visualización óptima de PDF. Personalice los diseños de página para una mejor legibilidad en cualquier lector de PDF.
type: docs
weight: 6290
url: /es/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Especifica el diseño de página que se utilizará cuando el documento se abra en un lector de PDF.

```csharp
public enum PdfPageLayout
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| SinglePage | `0` | Mostrar una página a la vez. |
| OneColumn | `1` | Mostrar las páginas en una columna. |
| TwoColumnLeft | `2` | Muestra las páginas en dos columnas, con las páginas impares a la izquierda. |
| TwoColumnRight | `3` | Muestra las páginas en dos columnas, con las páginas impares a la derecha. |
| TwoPageLeft | `4` | Muestra las páginas de dos en dos, con las páginas impares a la izquierda. |
| TwoPageRight | `5` | Muestra las páginas de dos en dos, con las páginas impares a la derecha. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
