---
title: TableStyle.ColumnStripe
second_title: Referencia de API de Aspose.Words para .NET
description: TableStyle propiedad. Obtiene o establece un número de columnas para incluir en las bandas cuando el estilo especifica bandas de columnas pares/impares.
type: docs
weight: 70
url: /es/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Obtiene o establece un número de columnas para incluir en las bandas cuando el estilo especifica bandas de columnas pares/impares.

```csharp
public int ColumnStripe { get; set; }
```

### Ejemplos

Muestra cómo crear estilos de tabla condicionales que alternan entre filas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Podemos configurar un estilo condicional de una tabla para aplicar un color diferente a la fila/columna,
// basado en si la fila/columna es par o impar, creando un patrón de color alterno.
// También podemos aplicar un número n a las bandas de fila/columna,
// lo que significa que el color se alterna después de cada n filas/columnas en lugar de una.
// Cree una tabla donde las columnas y filas individuales se agruparán en bandas y las columnas se agruparán en grupos de tres.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Aplicar un estilo de línea a todos los bordes de la tabla.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Establece los dos colores, que se alternarán cada 3 filas.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Establece un color para aplicar a cada columna par, lo que anulará cualquier color de fila personalizado.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// La propiedad "StyleOptions" habilita las bandas de filas de forma predeterminada.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Utilice la propiedad "StyleOptions" también para habilitar las bandas de columnas.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Ver también

* class [TableStyle](../)
* espacio de nombres [Aspose.Words](../../tablestyle/)
* asamblea [Aspose.Words](../../../)


