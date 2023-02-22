---
title: Table.AllowAutoFit
second_title: Referencia de API de Aspose.Words para .NET
description: Table propiedad. Permite que Microsoft Word y Aspose.Words cambien automáticamente el tamaño de las celdas de una tabla para que se ajusten a su contenido.
type: docs
weight: 50
url: /es/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Permite que Microsoft Word y Aspose.Words cambien automáticamente el tamaño de las celdas de una tabla para que se ajusten a su contenido.

```csharp
public bool AllowAutoFit { get; set; }
```

### Observaciones

El valor predeterminado es`verdadero`.

### Ejemplos

Muestra cómo habilitar/deshabilitar el redimensionamiento automático de celdas de tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Establecer la propiedad "AllowAutoFit" en "falso" para que la tabla mantenga las dimensiones
// de todas sus filas y celdas, y trunca el contenido si es demasiado grande para caber.
// Establezca la propiedad "AllowAutoFit" en "true" para permitir que la tabla cambie el ancho y el alto de sus celdas
// para acomodar su contenido.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../table/)
* asamblea [Aspose.Words](../../../)


