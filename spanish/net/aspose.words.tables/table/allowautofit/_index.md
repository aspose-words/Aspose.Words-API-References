---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words para .NET
description: Descubra la propiedad Table AllowAutoFit para cambiar sin esfuerzo el tamaño de las celdas de las tablas de Microsoft Word y Aspose.Words, mejorando la legibilidad y la presentación de su documento.
type: docs
weight: 50
url: /es/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Permite que Microsoft Word y Aspose.Words cambien automáticamente el tamaño de las celdas de una tabla para que se ajusten a su contenido.

```csharp
public bool AllowAutoFit { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero`.

## Ejemplos

Muestra cómo habilitar o deshabilitar el cambio de tamaño automático de las celdas de la tabla.

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

// Establezca la propiedad "AllowAutoFit" en "falso" para que la tabla mantenga las dimensiones
// de todas sus filas y celdas, y truncar el contenido si es demasiado grande para caber.
// Establezca la propiedad "AllowAutoFit" en "true" para permitir que la tabla cambie el ancho y la altura de sus celdas
// para acomodar su contenido.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
