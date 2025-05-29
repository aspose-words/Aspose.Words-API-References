---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words para .NET
description: Descubre el método CellFormat ClearFormatting para restablecer fácilmente los estilos de celda a sus valores predeterminados sin modificar el ancho. ¡Mejora la eficiencia de tus hojas de cálculo!
type: docs
weight: 160
url: /es/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Restablece el formato de celda predeterminado. No modifica el ancho de la celda.

```csharp
public void ClearFormatting()
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

* class [CellFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
