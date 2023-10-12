---
title: Class Row
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Tables.Row clase. Representa una fila de la tabla.
type: docs
weight: 6310
url: /es/net/aspose.words.tables/row/
---
## Row class

Representa una fila de la tabla.

Para obtener más información, visite el[Trabajar con tablas](https://docs.aspose.com/words/net/working-with-tables/) artículo de documentación.

```csharp
public class Row : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Row](row/)(DocumentBase) | Inicializa una nueva instancia del`Row` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Cells](../../aspose.words.tables/row/cells/) { get; } | Proporciona acceso escrito al[`Cell`](../cell/) nodos secundarios de la fila. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstCell](../../aspose.words.tables/row/firstcell/) { get; } | Devuelve el primero[`Cell`](../cell/) en la fila. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devoluciones`verdadero` si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devoluciones`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsFirstRow](../../aspose.words.tables/row/isfirstrow/) { get; } | Verdadero si esta es la primera fila de una tabla; falso en caso contrario. |
| [IsLastRow](../../aspose.words.tables/row/islastrow/) { get; } | Verdadero si esta es la última fila de una tabla; falso en caso contrario. |
| [LastCell](../../aspose.words.tables/row/lastcell/) { get; } | Devuelve el último[`Cell`](../cell/) en la fila. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [NextRow](../../aspose.words.tables/row/nextrow/) { get; } | Obtiene el siguiente`Row` nodo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.tables/row/nodetype/) { get; } | DevolucionesRow . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentTable](../../aspose.words.tables/row/parenttable/) { get; } | Devuelve la tabla principal inmediata de la fila. |
| [PreviousRow](../../aspose.words.tables/row/previousrow/) { get; } | Obtiene el anterior`Row` nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/) objeto que representa la parte de un documento contenido en este nodo. |
| [RowFormat](../../aspose.words.tables/row/rowformat/) { get; } | Proporciona acceso a las propiedades de formato de la fila. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.tables/row/accept/)(DocumentVisitor) | Acepta un visitante. |
| override [AcceptEnd](../../aspose.words.tables/row/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.tables/row/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que se puede utilizar para atravesar y leer nodos. |
| [EnsureMinimum](../../aspose.words.tables/row/ensureminimum/)() | Si el`Row` no tiene celdas, crea y agrega una[`Cell`](../cell/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer antepasado del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words.tables/row/gettext/)() | Obtiene el texto de todas las celdas de esta fila, incluido el carácter de final de fila. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/)nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selecciona el primero[`Node`](../../aspose.words/node/) que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

### Observaciones

`Row` sólo puede ser hijo de un[`Table`](../table/).

`Row` puede contener uno o más[`Cell`](../cell/) nodos.

Una fila mínima válida debe tener al menos una[`Cell`](../cell/).

### Ejemplos

Muestra cómo crear una tabla.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Las tablas contienen filas, que contienen celdas, que pueden tener párrafos
// con elementos típicos como corridas, formas e incluso otras tablas.
// Llamar al método "EnsureMinimum" en una tabla garantizará que
// la tabla tiene al menos una fila, una celda y un párrafo.
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

Muestra cómo crear una tabla anidada sin utilizar un generador de documentos.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Cree la tabla exterior con tres filas y cuatro columnas y luego agréguela al documento.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Crea otra tabla con dos filas y dos columnas y luego insértala en la primera celda de la primera tabla.
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

    // Puedes usar las propiedades "Título" y "Descripción" para agregar un título y una descripción respectivamente a tu tabla.
    // La tabla debe tener al menos una fila antes de que podamos usar estas propiedades.
    // Estas propiedades son significativas para documentos .docx compatibles con ISO/IEC 29500 (consulte la clase OoxmlCompliance).
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


