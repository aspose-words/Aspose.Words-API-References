---
title: Table.LeftPadding
second_title: Referencia de API de Aspose.Words para .NET
description: Table propiedad. Obtiene o establece la cantidad de espacio en puntos que se agrega a la izquierda del contenido de las celdas.
type: docs
weight: 200
url: /es/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la izquierda del contenido de las celdas.

```csharp
public double LeftPadding { get; set; }
```

### Ejemplos

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

// Para cada celda de la tabla, establezca la distancia entre su contenido y cada uno de sus bordes. 
// Esta tabla mantendrá la distancia de relleno mínima al envolver el texto.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../table/)
* asamblea [Aspose.Words](../../../)


