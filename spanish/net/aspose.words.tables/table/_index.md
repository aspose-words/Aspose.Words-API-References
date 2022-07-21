---
title: Table
second_title: Referencia de API de Aspose.Words para .NET
description: Representa una tabla en un documento de Word.
type: docs
weight: 6040
url: /es/net/aspose.words.tables/table/
---
## Table class

Representa una tabla en un documento de Word.

```csharp
public class Table : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Table](table)(DocumentBase) | Inicializa una nueva instancia del **Mesa** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance) { get; set; } | Obtiene o establece la posición absoluta de la tabla flotante horizontal especificada por las propiedades de la tabla, en puntos. El valor predeterminado es 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance) { get; set; } | Obtiene o establece la posición de la tabla flotante vertical absoluta especificada por las propiedades de la tabla, en puntos. El valor predeterminado es 0. |
| [Alignment](../../aspose.words.tables/table/alignment) { get; set; } | Especifica cómo se alinea una tabla en línea en el documento. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit) { get; set; } | Permite que Microsoft Word y Aspose.Words cambien automáticamente el tamaño de las celdas de una tabla para que se ajusten a su contenido. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing) { get; set; } | Obtiene o establece la opción "Permitir espacio entre celdas". |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap) { get; } | Obtiene si una tabla flotante permitirá que otros objetos flotantes en el documento superpongan sus extensiones cuando se muestre. El valor predeterminado es`verdadero` . |
| [Bidi](../../aspose.words.tables/table/bidi) { get; set; } | Obtiene o establece si se trata de una tabla de derecha a izquierda. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) para agregar debajo del contenido de las celdas. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) entre las celdas. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| [Description](../../aspose.words.tables/table/description) { get; set; } | Obtiene o establece la descripción de esta tabla. Proporciona una representación de texto alternativa de la información contenida en la tabla. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom) { get; } | Obtiene la distancia entre la parte inferior de la tabla y el texto circundante, en puntos. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft) { get; } | Obtiene la distancia entre la izquierda de la tabla y el texto circundante, en puntos. |
| [DistanceRight](../../aspose.words.tables/table/distanceright) { get; } | Obtiene la distancia entre la derecha de la tabla y el texto circundante, en puntos. |
| [DistanceTop](../../aspose.words.tables/table/distancetop) { get; } | Obtiene la distancia entre la parte superior de la mesa y el texto circundante, en puntos. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtiene el primer hijo del nodo. |
| [FirstRow](../../aspose.words.tables/table/firstrow) { get; } | Devuelve el primero **Fila** nodo en la tabla. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor) { get; set; } | Obtiene el objeto base a partir del cual se debe calcular el posicionamiento horizontal de la tabla flotante. El valor predeterminado esColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtiene el último hijo del nodo. |
| [LastRow](../../aspose.words.tables/table/lastrow) { get; } | Devuelve el último **Fila** nodo en la tabla. |
| [LeftIndent](../../aspose.words.tables/table/leftindent) { get; set; } | Obtiene o establece el valor que representa la sangría izquierda de la tabla. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la izquierda del contenido de las celdas. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.tables/table/nodetype) { get; } | Devoluciones **NodeType.Table** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth) { get; set; } | Obtiene o establece el ancho preferido de la tabla. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment) { get; set; } | Obtiene o establece la alineación horizontal relativa de la tabla flotante. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment) { get; set; } | Obtiene o establece la alineación vertical relativa de la tabla flotante. |
| [RightPadding](../../aspose.words.tables/table/rightpadding) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la derecha del contenido de las celdas. |
| [Rows](../../aspose.words.tables/table/rows) { get; } | Proporciona acceso escrito a las filas de la tabla. |
| [Style](../../aspose.words.tables/table/style) { get; set; } | Obtiene o establece el estilo de tabla aplicado a esta tabla. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier) { get; set; } | Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de tabla aplicado a esta tabla. |
| [StyleName](../../aspose.words.tables/table/stylename) { get; set; } | Obtiene o establece el nombre del estilo de tabla aplicado a esta tabla. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions) { get; set; } | Obtiene o establece indicadores de bits que especifican cómo se aplica un estilo de tabla a esta tabla. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping) { get; set; } | Obtiene o establece[`TextWrapping`](./textwrapping) para tabla. |
| [Title](../../aspose.words.tables/table/title) { get; set; } | Obtiene o establece el título de esta tabla. Proporciona una representación de texto alternativa de la información contenida en la tabla. |
| [TopPadding](../../aspose.words.tables/table/toppadding) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará encima del contenido de las celdas. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor) { get; set; } | Obtiene el objeto base a partir del cual se debe calcular el posicionamiento vertical de la tabla flotante. El valor predeterminado esMargin . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AutoFit](../../aspose.words.tables/table/autofit)(AutoFitBehavior) | Cambia el tamaño de la tabla y las celdas según el comportamiento de ajuste automático especificado. |
| [ClearBorders](../../aspose.words.tables/table/clearborders)() | Elimina todos los bordes de tablas y celdas de esta tabla. |
| [ClearShading](../../aspose.words.tables/table/clearshading)() | Elimina todo el sombreado de la mesa. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicado del nodo. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells)() | Convierte celdas fusionadas horizontalmente por ancho en celdas fusionadas por[`HorizontalMerge`](../cellformat/horizontalmerge) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reservado para uso del sistema. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum)() | Si la tabla no tiene filas, crea y agrega una **Fila** . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder)(BorderType, LineStyle, double, Color, bool) | Establece el borde de la tabla especificado en el estilo de línea, el ancho y el color especificados. |
| [SetBorders](../../aspose.words.tables/table/setborders)(LineStyle, double, Color) | Establece todos los bordes de la tabla en el estilo de línea, el ancho y el color especificados. |
| [SetShading](../../aspose.words.tables/table/setshading)(TextureIndex, Color, Color) | Establece el sombreado a los valores especificados en toda la tabla. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

**Mesa**es un nodo a nivel de bloque y puede ser un hijo de clases derivadas de **Historia** or  **Historia en línea**.

**Mesa** puede contener uno o más **Fila** nodos.

Una tabla válida mínima debe tener al menos una **Fila**.

### Ejemplos

Muestra cómo crear una tabla.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Las tablas contienen filas, que contienen celdas, que pueden tener párrafos
// con elementos típicos como carreras, formas e incluso otras tablas.
// Llamar al método "EnsureMinimum" en una tabla asegurará que
// la tabla tiene al menos una fila, celda y párrafo.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Agrega texto a la primera llamada en la primera fila de la tabla.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Muestra cómo recorrer todas las tablas del documento e imprimir el contenido de cada celda.

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

Muestra cómo crear una tabla de 2x2 con formato.

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

// Mientras crea la tabla, el generador de documentos aplicará sus valores de propiedad RowFormat/CellFormat actuales
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

// Las filas y celdas añadidas previamente no se ven afectadas retroactivamente por los cambios en el formato del constructor.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Muestra cómo crear una tabla anidada sin utilizar un generador de documentos.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Cree la tabla exterior con tres filas y cuatro columnas y luego agréguela al documento.
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

    // Puede usar las propiedades "Título" y "Descripción" para agregar un título y una descripción respectivamente a su tabla.
    // La tabla debe tener al menos una fila antes de que podamos usar estas propiedades.
    // Estas propiedades son significativas para documentos .docx compatibles con ISO/IEC 29500 (consulte la clase OoxmlCompliance).
    // Si guardamos el documento en formatos anteriores a ISO/IEC 29500, Microsoft Word ignora estas propiedades.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ver también

* class [CompositeNode](../../aspose.words/compositenode)
* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
