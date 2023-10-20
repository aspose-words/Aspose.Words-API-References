---
title: Table.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words para .NET
description: Table LeftPadding propiedad. Obtiene o establece la cantidad de espacio en puntos que se agregará a la izquierda del contenido de las celdas en C#.
type: docs
weight: 200
url: /es/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Obtiene o establece la cantidad de espacio (en puntos) que se agregará a la izquierda del contenido de las celdas.

```csharp
public double LeftPadding { get; set; }
```

## Ejemplos

Muestra cómo configurar el relleno de contenido en una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Para cada celda de la tabla, establece la distancia entre su contenido y cada uno de sus bordes.
// Esta tabla mantendrá la distancia mínima de relleno ajustando el texto.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
