---
title: ConditionalStyle
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un formato especial aplicado a alguna área de una tabla con estilo de tabla asignado.
type: docs
weight: 300
url: /es/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Representa un formato especial aplicado a alguna área de una tabla con estilo de tabla asignado.

```csharp
public sealed class ConditionalStyle
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Obtiene la colección de bordes de celda predeterminados para el estilo condicional. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se debe agregar debajo del contenido de las celdas de la tabla. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Obtiene el formato de carácter del estilo condicional. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la izquierda del contenido de las celdas de la tabla. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Obtiene el formato de párrafo del estilo condicional. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la derecha del contenido de las celdas de la tabla. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Obtiene un[`Shading`](../shading/) objeto que hace referencia al formato de sombreado para este estilo condicional. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará encima del contenido de las celdas de la tabla. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Obtiene el área de la tabla con la que se relaciona este estilo condicional. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Borra el formato de este estilo condicional. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(object) |  |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Calcula el código hash para este objeto. |

### Ejemplos

Muestra cómo trabajar con determinados estilos de área de una tabla.

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
// basado en un predicado, como que las celdas estén en la última fila.
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

// Lista todas las condiciones de estilo posibles.
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

// Nuestro estilo aplica algunos estilos condicionales por defecto.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Tendremos que habilitar todos los demás estilos nosotros mismos a través de la propiedad "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
