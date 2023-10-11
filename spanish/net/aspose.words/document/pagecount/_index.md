---
title: Document.PageCount
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene el número de páginas del documento calculado mediante la operación de diseño de página más reciente.
type: docs
weight: 320
url: /es/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Obtiene el número de páginas del documento calculado mediante la operación de diseño de página más reciente.

```csharp
public int PageCount { get; }
```

### Ejemplos

Muestra cómo contar el número de páginas del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Verificar el recuento de páginas esperado del documento.
Assert.AreEqual(3, doc.PageCount);

// Obtener la propiedad PageCount invocó el diseño de página del documento para calcular el valor.
// No será necesario volver a realizar esta operación cuando se renderice el documento en un formato de guardado de página fijo,
// como .pdf. Así podrás ahorrar algo de tiempo, especialmente con documentos más complejos.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Ver también

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


