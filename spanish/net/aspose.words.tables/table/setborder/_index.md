---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words para .NET
description: Personaliza la apariencia de tu tabla con el método SetBorder ajusta el estilo, el ancho y el color de la línea para lograr un aspecto profesional. ¡Mejora tu diseño hoy mismo!
type: docs
weight: 430
url: /es/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Establece el borde de la tabla especificada con el estilo de línea, ancho y color especificados.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| borderType | BorderType | El borde de la tabla para cambiar. |
| lineStyle | LineStyle | El estilo de línea a aplicar. |
| lineWidth | Double | El ancho de línea a establecer (en puntos). |
| color | Color | El color a utilizar para el borde. |
| isOverrideCellBorders | Boolean | Cuando`verdadero`, hace que se eliminen todos los bordes de celda explícitos existentes. |

## Ejemplos

Muestra cómo aplicar un borde de contorno a una tabla.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Alinea la tabla al centro de la página.
table.Alignment = TableAlignment.Center;

//Borra todos los bordes y sombreados existentes de la tabla.
table.ClearBorders();
table.ClearShading();

//Añade bordes verdes al contorno de la tabla.
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
