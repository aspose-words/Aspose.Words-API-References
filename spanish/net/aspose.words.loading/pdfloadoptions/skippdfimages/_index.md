---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words para .NET
description: PdfLoadOptions SkipPdfImages propiedad. Obtiene o establece el indicador que indica si se deben omitir las imágenes al cargar el documento PDF. El valor predeterminado esFALSO  en C#.
type: docs
weight: 40
url: /es/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Obtiene o establece el indicador que indica si se deben omitir las imágenes al cargar el documento PDF. El valor predeterminado es`FALSO` .

```csharp
public bool SkipPdfImages { get; set; }
```

## Ejemplos

Muestra cómo omitir imágenes durante la carga de archivos PDF.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
{
    Assert.AreEqual(shapeCollection.Count, 0);
}
else
{
    Assert.AreNotEqual(shapeCollection.Count, 0);
}
```

### Ver también

* class [PdfLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
