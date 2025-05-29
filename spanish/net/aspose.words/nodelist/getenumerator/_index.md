---
title: NodeList.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Itera fácilmente NodeList con el método GetEnumerator. Disfruta de un acceso sencillo y eficiente a tu colección de nodos en C#.
type: docs
weight: 30
url: /es/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Valor_devuelto

Un IEnumerator.

## Ejemplos

Muestra cómo seleccionar ciertos nodos mediante una expresión XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Esta expresión extraerá todos los nodos del párrafo,
// que son descendientes de cualquier nodo de tabla en el documento.
NodeList nodeList = doc.SelectNodes("//Tabla//Párrafo");

// Itera a través de la lista con un enumerador e imprime el contenido de cada párrafo en cada celda de la tabla.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Esta expresión seleccionará cualquier párrafo que sea hijo directo de cualquier nodo Cuerpo en el documento.
nodeList = doc.SelectNodes("//Cuerpo/Párrafo");

//Podemos tratar la lista como una matriz.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Utilice SelectSingleNode para seleccionar el primer resultado de la misma expresión que la anterior.
Node node = doc.SelectSingleNode("//Cuerpo/Párrafo");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Ver también

* class [Node](../../node/)
* class [NodeList](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
