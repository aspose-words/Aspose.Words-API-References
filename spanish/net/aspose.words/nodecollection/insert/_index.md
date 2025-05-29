---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words para .NET
description: Inserte nodos fácilmente en su NodeCollection en cualquier índice con nuestro método de inserción optimizado. ¡Mejore su gestión de datos hoy mismo!
type: docs
weight: 80
url: /es/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Inserta un nodo en la colección en el índice especificado.

```csharp
public void Insert(int index, Node node)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice basado en cero del nodo. Se permiten índices negativos e indican acceso desde el final de la lista. Por ejemplo, -1 significa el último nodo, -2 significa el segundo antes del último y así sucesivamente. |
| node | Node | El nodo a insertar. |

### Excepciones

| excepción | condición |
| --- | --- |
| NotSupportedException | El[`NodeCollection`](../) es una colección "profunda". |

## Observaciones

El nodo se inserta como un elemento secundario en el objeto de nodo desde el cual se creó la colección.

Si el índice es igual o mayor que[`Count`](../count/), el nodo se agrega al final de la colección.

Si el índice es negativo y su valor absoluto es mayor que[`Count`](../count/), el nodo se agrega al final de la colección.

Si el nodo que se está insertando se creó a partir de otro documento, debe utilizar [`ImportNode`](../../documentbase/importnode/) para importar el nodo al documento actual. Luego, el nodo importado se puede insertar en el documento actual.

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
