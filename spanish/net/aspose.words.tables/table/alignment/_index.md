---
title: Table.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words para .NET
description: Descubra la propiedad Alineación de tabla para controlar sin esfuerzo la posición de la tabla en línea en sus documentos para lograr una apariencia pulida y profesional.
type: docs
weight: 40
url: /es/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

Especifica cómo se alinea una tabla en línea en el documento.

```csharp
public TableAlignment Alignment { get; set; }
```

## Observaciones

El valor predeterminado esLeft.

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

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
