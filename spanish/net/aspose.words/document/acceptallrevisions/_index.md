---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words para .NET
description: Agilice su proceso de edición con el método AcceptAllRevisions, aceptando sin esfuerzo todos los cambios rastreados en su documento para obtener una versión final pulida.
type: docs
weight: 540
url: /es/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Acepta todos los cambios rastreados en el documento.

```csharp
public void AcceptAllRevisions()
```

## Observaciones

Este método es un atajo para[`AcceptAll`](../../revisioncollection/acceptall/).

## Ejemplos

Muestra cómo aceptar todos los cambios de seguimiento en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Edite el documento mientras realiza el seguimiento de los cambios para crear algunas revisiones.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! ");
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Podemos iterar a través de cada revisión y aceptarla/rechazarla como parte de nuestro documento.
// Si sabemos que deseamos aceptar cada revisión, podemos hacerlo de manera más directa llamando a este método.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
