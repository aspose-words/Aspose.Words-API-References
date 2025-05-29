---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words para .NET
description: Descubra si un CompositeNode tiene nodos secundarios con la propiedad HasChildNodes. Simplifique su codificación con esta función esencial para una gestión eficiente de nodos.
type: docs
weight: 30
url: /es/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Devuelve`verdadero` si este nodo tiene nodos secundarios.

```csharp
public bool HasChildNodes { get; }
```

## Ejemplos

Muestra cómo combinar las filas de dos tablas en una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

A continuación se muestran dos formas de obtener una tabla de un documento.
// 1 - De la colección "Tablas" de un nodo Cuerpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Usando el método "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Agrega todas las filas de la tabla actual a la siguiente.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

//Eliminar el contenedor de tabla vacío.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Ver también

* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
