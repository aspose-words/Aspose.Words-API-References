---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Tables.TableAlignment para una alineación óptima de tablas en línea. Mejore el formato de sus documentos con precisión y facilidad.
type: docs
weight: 7200
url: /es/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Especifica la alineación para una tabla en línea.

```csharp
public enum TableAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Left | `0` | La tabla está alineada a la izquierda. |
| Center | `1` | La mesa está centrada. |
| Right | `2` | La tabla está alineada a la derecha. |

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

* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)
