---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda fácilmente a nodos específicos con la propiedad NodeList Item. Recupere nodos por índice para una manipulación de datos optimizada y una codificación eficiente.
type: docs
weight: 20
url: /es/net/aspose.words/nodelist/item/
---
## NodeList indexer

Recupera un nodo en el índice dado.

```csharp
public Node this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice en la lista de nodos. |

## Observaciones

El índice está basado en cero.

Se permiten índices negativos e indican acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos de la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que la cantidad de elementos de la lista, esto devuelve una referencia nula.

## Ejemplos

Muestra cómo utilizar XPaths para navegar por una lista de nodos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte algunos nodos con un DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

//Nuestro documento contiene tres nodos de ejecución.
NodeList nodeList = doc.SelectNodes("//Correr");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Utilice una barra diagonal doble para seleccionar todos los nodos de ejecución
// que son descendientes indirectos de un nodo Tabla, que serían las ejecuciones dentro de las dos celdas que insertamos.
nodeList = doc.SelectNodes("//Table//Correr");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Las barras diagonales simples especifican relaciones de descendientes directos,
// que omitimos cuando usamos barras dobles.
Assert.AreEqual(doc.SelectNodes(" //Tabla//Ejecutar"),
    doc.SelectNodes("//Tabla/Fila/Celda/Párrafo/Ejecutar"));

// Accedemos a la forma que contiene la imagen que insertamos.
nodeList = doc.SelectNodes("//Forma");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Ver también

* class [Node](../../node/)
* class [NodeList](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
