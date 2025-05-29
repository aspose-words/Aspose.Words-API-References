---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words para .NET
description: Descubra PdfLoadOptions PageIndex. Configure fácilmente el índice de la página inicial para la lectura de PDF con esta propiedad flexible. ¡Optimice la gestión de sus PDF hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

Obtiene o establece el índice (basado en 0) de la primera página a leer. El valor predeterminado es 0.

```csharp
public int PageIndex { get; set; }
```

## Ejemplos

Muestra cómo omitir imágenes durante la carga de archivos PDF.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### Ver también

* class [PdfLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
