---
title: TextureIndex Enum
linktitle: TextureIndex
articleTitle: TextureIndex
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.TextureIndex para texturas de sombreado avanzadas. Mejore el diseño de sus documentos con texturas personalizables de alta calidad.
type: docs
weight: 7300
url: /es/net/aspose.words/textureindex/
---
## TextureIndex enumeration

Especifica la textura del sombreado.

```csharp
public enum TextureIndex
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Texture10Percent | `3` |  |
| Texture12Pt5Percent | `37` |  |
| Texture15Percent | `38` |  |
| Texture17Pt5Percent | `39` |  |
| Texture20Percent | `4` |  |
| Texture22Pt5Percent | `40` |  |
| Texture25Percent | `5` |  |
| Texture27Pt5Percent | `41` |  |
| Texture2Pt5Percent | `35` |  |
| Texture30Percent | `6` |  |
| Texture32Pt5Percent | `42` |  |
| Texture35Percent | `43` |  |
| Texture37Pt5Percent | `44` |  |
| Texture40Percent | `7` |  |
| Texture42Pt5Percent | `45` |  |
| Texture45Percent | `46` |  |
| Texture47Pt5Percent | `47` |  |
| Texture50Percent | `8` |  |
| Texture52Pt5Percent | `48` |  |
| Texture55Percent | `49` |  |
| Texture57Pt5Percent | `50` |  |
| Texture5Percent | `2` |  |
| Texture60Percent | `9` |  |
| Texture62Pt5Percent | `51` |  |
| Texture65Percent | `52` |  |
| Texture67Pt5Percent | `53` |  |
| Texture70Percent | `10` |  |
| Texture72Pt5Percent | `54` |  |
| Texture75Percent | `11` |  |
| Texture77Pt5Percent | `55` |  |
| Texture7Pt5Percent | `36` |  |
| Texture80Percent | `12` |  |
| Texture82Pt5Percent | `56` |  |
| Texture85Percent | `57` |  |
| Texture87Pt5Percent | `58` |  |
| Texture90Percent | `13` |  |
| Texture92Pt5Percent | `59` |  |
| Texture95Percent | `60` |  |
| Texture97Pt5Percent | `61` |  |
| TextureCross | `24` |  |
| TextureDarkCross | `18` |  |
| TextureDarkDiagonalCross | `19` |  |
| TextureDarkDiagonalDown | `16` |  |
| TextureDarkDiagonalUp | `17` |  |
| TextureDarkHorizontal | `14` |  |
| TextureDarkVertical | `15` |  |
| TextureDiagonalCross | `25` |  |
| TextureDiagonalDown | `22` |  |
| TextureDiagonalUp | `23` |  |
| TextureHorizontal | `20` |  |
| TextureNone | `0` |  |
| TextureSolid | `1` |  |
| TextureVertical | `21` |  |
| TextureNil | `65535` | Especifica que no se utilizará ningún patrón en la región sombreada actual (es decir, el patrón será un relleno completo con el color de fondo). |

## Ejemplos

Muestra cómo decorar texto con bordes y sombreado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
