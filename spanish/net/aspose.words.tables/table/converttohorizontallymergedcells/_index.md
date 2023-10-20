---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words para .NET
description: Table ConvertToHorizontallyMergedCells método. Convierte celdas fusionadas horizontalmente por ancho en celdas fusionadas porHorizontalMerge  en C#.
type: docs
weight: 390
url: /es/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Convierte celdas fusionadas horizontalmente por ancho en celdas fusionadas por[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## Observaciones

Las celdas de la tabla se pueden combinar horizontalmente usando indicadores de combinación[`HorizontalMerge`](../../cellformat/horizontalmerge/) o usando el ancho de celda[`Width`](../../cellformat/width/).

Cuando la celda de la tabla se combina con la propiedad de ancho[`HorizontalMerge`](../../cellformat/horizontalmerge/) No tiene sentido, pero a veces tener indicadores de combinación es una forma más conveniente.

Utilice este método para transformar celdas de tabla fusionadas horizontalmente por ancho en celdas fusionadas mediante indicadores de combinación.

## Ejemplos

Muestra cómo convertir celdas fusionadas horizontalmente por ancho en celdas fusionadas por CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word ya no escribe indicadores de combinación, sino que define las celdas combinadas por ancho.
// Aspose.Words define de forma predeterminada solo 5 celdas seguidas y ninguna de ellas tiene el indicador de combinación horizontal,
// a pesar de que había 7 celdas en la fila antes de que se produjera la fusión horizontal.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Utilice el método "ConvertToHorizontallyMergedCells" para convertir celdas fusionadas horizontalmente
// por su ancho a la celda fusionada horizontalmente por banderas.
// Ahora tenemos 7 celdas y algunas de ellas tienen valores de combinación horizontal.
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.AreEqual(7, row.Cells.Count);

Assert.AreEqual(CellMerge.None, row.Cells[0].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[1].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[2].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[3].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[4].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[5].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[6].CellFormat.HorizontalMerge);
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
