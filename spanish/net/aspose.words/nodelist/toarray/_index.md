---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words para .NET
description: Convierta sin esfuerzo NodeList en una matriz con el método ToArray, simplificando la manipulación de nodos y mejorando su flujo de trabajo de desarrollo web.
type: docs
weight: 40
url: /es/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

Copia todos los nodos de la colección a una nueva matriz de nodos.

```csharp
public Node[] ToArray()
```

### Valor_devuelto

Una matriz de nodos.

## Observaciones

No debe agregar o quitar nodos mientras itera sobre una colección de nodos porque invalida el iterador y requiere actualizaciones para las colecciones en vivo.

Para poder agregar o quitar nodos durante la iteración, utilice este método para copiar nodos en una matriz de tamaño fijo y luego iterar sobre la matriz.

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
