---
title: NodeList.Item
second_title: Referencia de API de Aspose.Words para .NET
description: NodeList propiedad. Recupera un nodo en el índice dado.
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

### Observaciones

El índice tiene base cero.

Se permiten índices negativos e indican el acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos de la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos de la lista, esto devuelve una referencia nula.

### Ejemplos

Muestra cómo utilizar XPaths para navegar en una NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta algunos nodos con un DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

#if NET48 || JAVA
builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
#elif NET5_0_OR_GREATER || __MOBILE__
using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(image);
#endif

// Nuestro documento contiene tres nodos Ejecutar.
NodeList nodeList = doc.SelectNodes("//Correr");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Utilice una doble barra diagonal para seleccionar todos los nodos de ejecución
// que son descendientes indirectos de un nodo Tabla, que serían las ejecuciones dentro de las dos celdas que insertamos.
nodeList = doc.SelectNodes("//Table//Correr");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Las barras diagonales simples especifican relaciones descendientes directas,
// que omitimos cuando usamos barras dobles.
Assert.AreEqual(doc.SelectNodes(" //Tabla//Ejecutar"),
    doc.SelectNodes("//Tabla/Fila/Celda/Párrafo/Ejecutar"));

// Accede a la forma que contiene la imagen que insertamos.
nodeList = doc.SelectNodes("//Forma");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Ver también

* class [Node](../../node/)
* class [NodeList](../)
* espacio de nombres [Aspose.Words](../../nodelist/)
* asamblea [Aspose.Words](../../../)


