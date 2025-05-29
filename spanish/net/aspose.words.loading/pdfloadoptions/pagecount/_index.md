---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words para .NET
description: Controle la lectura de páginas con la propiedad PageCount de PdfLoadOptions. Configure fácilmente el número de páginas a leer, garantizando una gestión eficiente de los documentos.
type: docs
weight: 20
url: /es/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

Obtiene o establece el número de páginas a leer. El valor predeterminado es MaxValue, lo que significa que se leerán todas las páginas del documento.

```csharp
public int PageCount { get; set; }
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
