---
title: Table.RelativeVerticalAlignment
second_title: Referencia de API de Aspose.Words para .NET
description: Table propiedad. Obtiene o establece la alineación vertical relativa de la tabla flotante.
type: docs
weight: 240
url: /es/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Obtiene o establece la alineación vertical relativa de la tabla flotante.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
```

### Ejemplos

Muestra cómo configurar la ubicación de las tablas flotantes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Establece la ubicación de la tabla en un lugar de la página, como, en este caso, la esquina inferior derecha.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // También podemos establecer un desplazamiento horizontal y vertical en puntos desde la ubicación del párrafo donde insertamos la tabla.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Ver también

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../table/)
* asamblea [Aspose.Words](../../../)


