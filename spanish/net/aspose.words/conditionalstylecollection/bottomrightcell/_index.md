---
title: ConditionalStyleCollection.BottomRightCell
linktitle: BottomRightCell
articleTitle: BottomRightCell
second_title: Aspose.Words para .NET
description: Descubre la propiedad BottomRightCell en ConditionalStyleCollection. ¡Mejora tu diseño con estilos de celda personalizables para un mayor impacto visual!
type: docs
weight: 20
url: /es/net/aspose.words/conditionalstylecollection/bottomrightcell/
---
## ConditionalStyleCollection.BottomRightCell property

Obtiene el estilo de celda inferior derecha.

```csharp
public ConditionalStyle BottomRightCell { get; }
```

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

* class [ConditionalStyle](../../conditionalstyle/)
* class [ConditionalStyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
