---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words para .NET
description: Table SetBorder método. Establece el borde de la tabla especificado con el estilo ancho y color de línea especificados en C#.
type: docs
weight: 410
url: /es/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Establece el borde de la tabla especificado con el estilo, ancho y color de línea especificados.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| borderType | BorderType | El borde de la tabla para cambiar. |
| lineStyle | LineStyle | El estilo de línea que se aplicará. |
| lineWidth | Double | El ancho de línea a establecer (en puntos). |
| color | Color | El color que se utilizará para el borde. |
| isOverrideCellBorders | Boolean | Cuando`verdadero`, hace que se eliminen todos los bordes de celda explícitos existentes. |

## Ejemplos

Muestra cómo aplicar un borde de contorno a una tabla.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Alinea la tabla con el centro de la página.
table.Alignment = TableAlignment.Center;

// Borra los bordes y sombreados existentes de la tabla.
table.ClearBorders();
table.ClearShading();

// Agrega bordes verdes al contorno de la tabla.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Rellena las celdas con un color sólido verde claro.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Ver también

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
