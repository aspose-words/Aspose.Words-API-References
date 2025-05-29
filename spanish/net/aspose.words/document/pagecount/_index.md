---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words para .NET
description: Descubra la propiedad Document PageCount, que revela el recuento total de páginas según el último diseño, lo que garantiza una gestión y una información precisas de los documentos.
type: docs
weight: 330
url: /es/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Obtiene el número de páginas del documento calculado por la operación de diseño de página más reciente.

```csharp
public int PageCount { get; }
```

## Ejemplos

Muestra cómo contar el número de páginas del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Verificar el número de páginas esperado del documento.
Assert.AreEqual(3, doc.PageCount);

// Al obtener la propiedad PageCount se invoca el diseño de página del documento para calcular el valor.
// No será necesario volver a realizar esta operación al renderizar el documento en un formato de guardado de página fijo.
// como .pdf. Así puedes ahorrar tiempo, especialmente con documentos más complejos.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Ver también

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
