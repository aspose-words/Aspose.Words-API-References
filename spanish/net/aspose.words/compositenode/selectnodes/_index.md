---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words para .NET
description: Recupere nodos sin esfuerzo con el método CompositeNode SelectNodes usando expresiones XPath para una mejor manipulación de datos y una codificación optimizada.
type: docs
weight: 210
url: /es/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

Selecciona una lista de nodos que coinciden con la expresión XPath.

```csharp
public NodeList SelectNodes(string xpath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| xpath | String | La expresión XPath. |

### Valor_devuelto

Una lista de nodos que coinciden con la consulta XPath.

## Observaciones

Actualmente, solo se admiten expresiones con nombres de elementos. Las expresiones Expressions que utilizan nombres de atributos no son compatibles.

## Ejemplos

Muestra cómo utilizar una expresión XPath para probar si un nodo está dentro de un campo.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// La NodeList que resulta de esta expresión XPath contendrá todos los nodos que encontremos dentro de un campo.
// Sin embargo, los nodos FieldStart y FieldEnd pueden estar en la lista si hay campos anidados en la ruta.
// Actualmente no se encuentran campos raros en los que el FieldCode o FieldResult se extiende a lo largo de varios párrafos.
NodeList resultList =
    doc.SelectNodes("//CampoInicio/hermano-siguiente::nodo()[hermano-siguiente::FinCampo]");

// Verifica si la ejecución especificada es uno de los nodos que están dentro del campo.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
