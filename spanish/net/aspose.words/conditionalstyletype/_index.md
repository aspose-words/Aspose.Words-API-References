---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.ConditionalStyleType para definir el formato dinámico de tablas. Mejore los estilos de sus documentos con opciones condicionales flexibles.
type: docs
weight: 530
url: /es/net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

Representa posibles áreas de tabla en las que se puede definir formato condicional en un estilo de tabla.

```csharp
public enum ConditionalStyleType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FirstRow | `0` | Especifica el formato de la primera fila de una tabla. |
| FirstColumn | `1` | Especifica el formato de la primera columna de una tabla. |
| LastRow | `2` | Especifica el formato de la última fila de una tabla. |
| LastColumn | `3` | Especifica el formato de la última columna de una tabla. |
| OddRowBanding | `4` | Especifica el formato de la franja de fila impar. |
| OddColumnBanding | `5` | Especifica el formato de la franja de columna de número impar. |
| EvenRowBanding | `6` | Especifica el formato de la franja de fila de número par. |
| EvenColumnBanding | `7` | Especifica el formato de la franja de columna de número par. |
| TopLeftCell | `8` | Especifica el formato de la celda superior izquierda de una tabla. |
| TopRightCell | `9` | Especifica el formato de la celda superior derecha de una tabla. |
| BottomLeftCell | `10` | Especifica el formato de la celda inferior izquierda de una tabla. |
| BottomRightCell | `11` | Especifica el formato de la celda inferior derecha de una tabla. |

## Ejemplos

Muestra cómo trabajar con ciertos estilos de área de una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Crea un estilo de tabla personalizado.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Los estilos condicionales son cambios de formato que afectan solo a algunas de las celdas de la tabla
// basado en un predicado, como por ejemplo que las celdas estén en la última fila.
// A continuación se muestran tres formas de acceder a los estilos condicionales de un estilo de tabla desde la colección "ConditionalStyles".
// 1 - Por tipo de estilo:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Por índice:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Como propiedad:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Aplicar relleno y formato de texto a estilos condicionales.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Enumere todas las posibles condiciones de estilo.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Aplicar el estilo personalizado, que contiene todos los estilos condicionales, a la tabla.
table.Style = tableStyle;

//Nuestro estilo aplica algunos estilos condicionales por defecto.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Necesitaremos habilitar todos los demás estilos nosotros mismos a través de la propiedad "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
