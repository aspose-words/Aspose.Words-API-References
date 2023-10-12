---
title: Class Shading
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Shading clase. Contiene atributos de sombreado para un objeto.
type: docs
weight: 5990
url: /es/net/aspose.words/shading/
---
## Shading class

Contiene atributos de sombreado para un objeto.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) artículo de documentación.

```csharp
public class Shading : InternableComplexAttr
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Obtiene o establece el color que se aplica al fondo del`Shading` objeto. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Obtiene o establece el color del tema del patrón de fondo en el esquema de color aplicado que está asociado con este`Shading` objeto. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Obtiene o establece un valor doble que aclara u oscurece el color de un tema de fondo. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Obtiene o establece el color que se aplica al primer plano del`Shading` objeto. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Obtiene o establece el color del tema del patrón de primer plano en el esquema de color aplicado que está asociado con este`Shading` objeto. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Obtiene o establece un valor doble que aclara u oscurece el color de un tema de primer plano. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Obtiene o establece la textura de sombreado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Elimina el sombreado del objeto. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(object) | Determina si el objeto especificado tiene el mismo valor que el objeto actual. |
| [Equals](../../aspose.words/shading/equals/#equals)(Shading) | Determina si el especificado`Shading` es igual en valor a la corriente`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Sirve como función hash para este tipo. |

### Ejemplos

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

Muestra cómo aplicar colores de borde y sombreado mientras construye una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inicia una tabla y establece un color/grosor predeterminado para sus bordes.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Crea una fila con dos celdas con diferentes colores de fondo.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Restablecer el formato de celda para deshabilitar los colores de fondo
// establece un grosor de borde personalizado para todas las celdas nuevas creadas por el constructor,
// luego construye una segunda fila.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Ver también

* class [InternableComplexAttr](../internablecomplexattr/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


