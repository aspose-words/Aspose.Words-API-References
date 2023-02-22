---
title: CompositeNode.SelectSingleNode
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode método. Selecciona el primer nodo que coincide con la expresión XPath.
type: docs
weight: 210
url: /es/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Selecciona el primer nodo que coincide con la expresión XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xpath | String | La expresión XPath. |

### Valor_devuelto

El primer nodo que coincide con la consulta XPath o nulo si no se encuentra ningún nodo coincidente.

### Observaciones

Por el momento, solo se admiten expresiones con nombres de elementos. No se admiten las expresiones que usan nombres de atributos.

### Ejemplos

Muestra cómo seleccionar determinados nodos mediante una expresión XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Esta expresión extraerá todos los nodos de párrafo,
// que son descendientes de cualquier nodo de tabla en el documento.
NodeList nodeList = doc.SelectNodes("//Tabla//Párrafo");

// Iterar a través de la lista con un enumerador e imprimir el contenido de cada párrafo en cada celda de la tabla.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Esta expresión seleccionará cualquier párrafo que sea hijo directo de cualquier nodo Cuerpo del documento.
nodeList = doc.SelectNodes("//Cuerpo del párrafo");

// Podemos tratar la lista como una matriz.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Use SelectSingleNode para seleccionar el primer resultado de la misma expresión anterior.
Node node = doc.SelectSingleNode("//Cuerpo del párrafo");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Ver también

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../compositenode/)
* asamblea [Aspose.Words](../../../)


