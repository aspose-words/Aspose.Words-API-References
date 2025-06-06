---
title: NodeCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words para .NET
description: Elimine sin esfuerzo nodos de su documento con el método NodeCollection Remove, agilizando la gestión de datos y mejorando el rendimiento.
type: docs
weight: 90
url: /es/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

Elimina el nodo de la colección y del documento.

```csharp
public void Remove(Node node)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| node | Node | El nodo a eliminar. |

## Ejemplos

Muestra cómo trabajar con una NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue texto al documento insertando ejecuciones usando un DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Cada invocación del método "Write" crea una nueva ejecución,
// que luego aparece en la RunCollection del párrafo padre.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// También podemos insertar un nodo en RunCollection manualmente.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Acceda a ejecuciones individuales y elimínelas para eliminar su texto del documento.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Ver también

* class [Node](../../node/)
* class [NodeCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
