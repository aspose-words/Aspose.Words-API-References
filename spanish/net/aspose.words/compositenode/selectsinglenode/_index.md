---
title: CompositeNode.SelectSingleNode
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode método. Selecciona el primeroNode que coincide con la expresión XPath.
type: docs
weight: 220
url: /es/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Selecciona el primero[`Node`](../../node/) que coincide con la expresión XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xpath | String | La expresión XPath. |

### Valor_devuelto

La primera[`Node`](../../node/) que coincida con la consulta XPath o`nulo` si no se encuentra ningún nodo coincidente.

### Observaciones

Por el momento, solo se admiten expresiones con nombres de elementos. No se admiten expresiones que utilizan nombres de atributos.

### Ejemplos

Muestra cómo seleccionar ciertos nodos mediante una expresión XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Esta expresión extraerá todos los nodos de párrafo,
// que son descendientes de cualquier nodo de tabla en el documento.
NodeList nodeList = doc.SelectNodes("//Tabla//Párrafo");

// Recorre la lista con un enumerador e imprime el contenido de cada párrafo en cada celda de la tabla.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Esta expresión seleccionará cualquier párrafo que sea hijo directo de cualquier nodo Cuerpo del documento.
nodeList = doc.SelectNodes("//Cuerpo del párrafo");

// Podemos tratar la lista como una matriz.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Utilice SelectSingleNode para seleccionar el primer resultado de la misma expresión anterior.
Node node = doc.SelectSingleNode("//Cuerpo del párrafo");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Ver también

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../compositenode/)
* asamblea [Aspose.Words](../../../)


