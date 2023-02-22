---
title: Document.Clone
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Realiza una copia profunda delDocument .
type: docs
weight: 530
url: /es/net/aspose.words/document/clone/
---
## Document.Clone method

Realiza una copia profunda del[`Document`](../) .

```csharp
public Document Clone()
```

### Valor_devuelto

El documento clonado.

### Ejemplos

Muestra cómo realizar una clonación profunda de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// La clonación producirá un nuevo documento con el mismo contenido que el original,
// pero con una copia única de cada uno de los nodos del documento original.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


