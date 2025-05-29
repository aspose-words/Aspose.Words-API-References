---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Tables.Table para crear y administrar fácilmente tablas en documentos de Word, mejorando el diseño y la funcionalidad de su documento.
type: docs
weight: 7190
url: /es/net/aspose.words.tables/table/
---
## Table class

Representa una tabla en un documento de Word.

Para obtener más información, visite el[Trabajar con tablas](https://docs.aspose.com/words/net/working-with-tables/) Artículo de documentación.

```csharp
public class Table : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Inicializa una nueva instancia del`Table` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Obtiene o establece la posición absoluta de la tabla flotante horizontal especificada por las propiedades de la tabla, en puntos. El valor predeterminado es 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Obtiene o establece la posición de tabla flotante vertical absoluta especificada por las propiedades de la tabla, en puntos. El valor predeterminado es 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Especifica cómo se alinea una tabla en línea en el documento. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Permite que Microsoft Word y Aspose.Words cambien automáticamente el tamaño de las celdas de una tabla para que se ajusten a su contenido. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Obtiene o establece la opción "Permitir espaciado entre celdas". |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Obtiene si una tabla flotante debe permitir que otros objetos flotantes en el documento se superpongan a sus extensiones cuando se muestran. El valor predeterminado es`verdadero` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Obtiene o establece si se trata de una tabla de derecha a izquierda. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará debajo del contenido de las celdas. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) entre las celdas. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Obtiene o establece la descripción de esta tabla. Proporciona una representación de texto alternativa de la información contenida en la tabla. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Obtiene o establece la distancia entre la parte inferior de la tabla y el texto circundante, en puntos. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Obtiene o establece la distancia entre la izquierda de la tabla y el texto circundante, en puntos. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Obtiene o establece la distancia entre la tabla derecha y el texto circundante, en puntos. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Obtiene o establece la distancia entre la parte superior de la mesa y el texto circundante, en puntos. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Devuelve el primer[`Row`](../row/) nodo en la tabla. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve`verdadero` si este nodo tiene nodos secundarios. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Obtiene el objeto base desde el cual se debe calcular el posicionamiento horizontal de la tabla flotante. El valor predeterminado esColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve`verdadero` ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Devuelve el último[`Row`](../row/) nodo en la tabla. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Obtiene o establece el valor que representa la sangría izquierda de la tabla. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará a la izquierda del contenido de las celdas. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | DevuelveTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Obtiene o establece el ancho preferido de la tabla. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/)objeto que representa la porción de un documento que está contenida en este nodo. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Obtiene o establece la alineación horizontal relativa de la tabla flotante. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Obtiene o establece la alineación vertical relativa de la tabla flotante. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará a la derecha del contenido de las celdas. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Proporciona acceso tipificado a las filas de la tabla. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Obtiene o establece el estilo de tabla aplicado a esta tabla. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de tabla aplicado a esta tabla. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Obtiene o establece el nombre del estilo de tabla aplicado a esta tabla. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Obtiene o establece indicadores de bits que especifican cómo se aplica un estilo de tabla a esta tabla. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Obtiene o establece[`TextWrapping`](./textwrapping/) para la tabla. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Obtiene o establece el título de esta tabla. Proporciona una representación de texto alternativa de la información contenida en la tabla. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará sobre el contenido de las celdas. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Obtiene el objeto base desde el cual se debe calcular el posicionamiento vertical de la tabla flotante. El valor predeterminado esMargin . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante por visitar el final de la tabla. |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante por visitar el inicio de la tabla. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Redimensiona la tabla y las celdas según el comportamiento de ajuste automático especificado. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Elimina todos los bordes de tablas y celdas de esta tabla. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Elimina todo el sombreado de la tabla. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Convierte celdas fusionadas horizontalmente por ancho en celdas fusionadas por[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que puede utilizarse para recorrer y leer nodos. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Si la tabla no tiene filas, crea y agrega una[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Devuelve un nodo secundario N que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Agrega el nodo especificado al comienzo de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el nodo anterior según el algoritmo de recorrido del árbol de preorden. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selecciona el primer[`Node`](../../aspose.words/node/) que coincide con la expresión XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Establece el borde de la tabla especificada con el estilo de línea, ancho y color especificados. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Establece todos los bordes de la tabla con el estilo de línea, ancho y color especificados. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Establece el sombreado en los valores especificados en toda la tabla. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporta el contenido del nodo en una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo en una cadena utilizando las opciones de guardado especificadas. |

## Observaciones

`Table` es un nodo a nivel de bloque y puede ser un hijo de clases derivadas de[`Story`](../../aspose.words/story/) o [`InlineStory`](../../aspose.words/inlinestory/).

`Table` puede contener uno o más[`Row`](../row/) nodos.

Una tabla mínima válida debe tener al menos una[`Row`](../row/).

## Ejemplos

Muestra cómo crear una tabla.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Las tablas contienen filas, que contienen celdas, que pueden tener párrafos
// con elementos típicos como carreras, formas e incluso otras tablas.
// Llamar al método "EnsureMinimum" en una tabla garantizará que
//la tabla tiene al menos una fila, una celda y un párrafo.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Agrega texto a la primera celda de la primera fila de la tabla.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Muestra cómo iterar a través de todas las tablas del documento e imprimir el contenido de cada celda.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Podemos usar el método "ToArray" en una colección de filas para clonarla en una matriz.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Podemos usar el método "ToArray" en una colección de celdas para clonarla en una matriz.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

Muestra cómo construir una tabla formateada de 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Al construir la tabla, el generador de documentos aplicará sus valores de propiedad RowFormat/CellFormat actuales
// a la fila/celda actual en la que se encuentra el cursor y a cualquier fila/celda nueva a medida que las crea.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Las filas y celdas agregadas previamente no se ven afectadas retroactivamente por los cambios en el formato del generador.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Muestra cómo construir una tabla anidada sin utilizar un generador de documentos.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Cree la tabla externa con tres filas y cuatro columnas y luego agréguela al documento.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Cree otra tabla con dos filas y dos columnas y luego insértela en la primera celda de la primera tabla.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crea una nueva tabla en el documento con las dimensiones y el texto dados en cada celda.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Puede utilizar las propiedades "Título" y "Descripción" para agregar un título y una descripción respectivamente a su tabla.
    //La tabla debe tener al menos una fila antes de que podamos usar estas propiedades.
    // Estas propiedades son significativas para los documentos .docx compatibles con ISO/IEC 29500 (consulte la clase OoxmlCompliance).
    // Si guardamos el documento en formatos anteriores a ISO/IEC 29500, Microsoft Word ignora estas propiedades.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ver también

* class [CompositeNode](../../aspose.words/compositenode/)
* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)
