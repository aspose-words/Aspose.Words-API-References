---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words para .NET
description: Mejore la apariencia de su tabla con el método SetShading, que le permite aplicar valores de sombreado personalizados para una apariencia pulida y profesional.
type: docs
weight: 450
url: /es/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Establece el sombreado en los valores especificados en toda la tabla.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| texture | TextureIndex | La textura a aplicar. |
| foregroundColor | Color | El color de la textura. |
| backgroundColor | Color | El color del relleno de fondo. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
