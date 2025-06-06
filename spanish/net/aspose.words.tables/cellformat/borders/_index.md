---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words para .NET
description: Descubra la propiedad CellFormat Borders para acceder y personalizar colecciones de bordes de celdas para mejorar el diseño y la funcionalidad de las hojas de cálculo.
type: docs
weight: 10
url: /es/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Obtiene la colección de bordes de la celda.

```csharp
public BorderCollection Borders { get; }
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

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
