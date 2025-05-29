---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad NodeList Count para recuperar fácilmente el número total de nodos en su lista, mejorando la eficiencia de su desarrollo web.
type: docs
weight: 10
url: /es/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Obtiene el número de nodos en la lista.

```csharp
public int Count { get; }
```

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

* class [NodeList](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
