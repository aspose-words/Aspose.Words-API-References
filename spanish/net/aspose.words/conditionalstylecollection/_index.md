---
title: Class ConditionalStyleCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.ConditionalStyleCollection clase. Representa una colección deConditionalStyle objetos.
type: docs
weight: 320
url: /es/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Representa una colección de[`ConditionalStyle`](../conditionalstyle/) objetos.

Para obtener más información, visite el[Trabajar con tablas](https://docs.aspose.com/words/net/working-with-tables/) artículo de documentación.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Obtiene el estilo de celda inferior izquierda. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Obtiene el estilo de celda inferior derecha. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Obtiene el número de estilos condicionales en la colección. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Obtiene el estilo de bandas de columnas pares. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Obtiene el estilo de bandas de filas pares. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Obtiene el estilo de la primera columna. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Obtiene el estilo de la primera fila. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Recupera un[`ConditionalStyle`](../conditionalstyle/) objeto por tipo de estilo condicional. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Obtiene el estilo de la última columna. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Obtiene el estilo de la última fila. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Obtiene el estilo de bandas de columna impar. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Obtiene el estilo de bandas de fila impar. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Obtiene el estilo de celda superior izquierda. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Obtiene el estilo de celda superior derecha. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Borra todos los estilos condicionales del estilo de tabla. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los estilos condicionales de la colección. |

### Observaciones

No es posible agregar ni eliminar elementos de esta colección. Contiene un conjunto permanente de elementos: un elemento para cada valor del[`ConditionalStyleType`](../conditionalstyletype/) tipo de enumeración.

### Ejemplos

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

// Los estilos condicionales son cambios de formato que afectan sólo a algunas de las celdas de la tabla.
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

// Enumere todas las condiciones de estilo posibles.
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

// Nuestro estilo aplica algunos estilos condicionales de forma predeterminada.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Necesitaremos habilitar todos los demás estilos nosotros mismos a través de la propiedad "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Ver también

* class [ConditionalStyle](../conditionalstyle/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


