---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words para .NET
description: Descubra cómo el método SelectSingleNode de CompositeNode recupera eficientemente el primer nodo que coincide con su expresión XPath para un manejo optimizado de los datos.
type: docs
weight: 220
url: /es/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Selecciona el primer[`Node`](../../node/) que coincide con la expresión XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xpath | String | La expresión XPath. |

### Valor_devuelto

La primera[`Node`](../../node/) que coincida con la consulta XPath o`nulo` si no se encuentra ningún nodo coincidente.

## Observaciones

Actualmente, solo se admiten expresiones con nombres de elementos. Las expresiones Expressions que utilizan nombres de atributos no son compatibles.

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
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
