---
title: Cell
second_title: Referencia de API de Aspose.Words para .NET
description: Representa una celda de tabla.
type: docs
weight: 5940
url: /es/net/aspose.words.tables/cell/
---
## Cell class

Representa una celda de tabla.

```csharp
public class Cell : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Cell](cell)(DocumentBase) | Inicializa una nueva instancia del **Célula** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat) { get; } | Proporciona acceso a las propiedades de formato de la celda. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph) { get; } | Obtiene el primer párrafo entre los hijos inmediatos. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell) { get; } | Verdadero si esta es la primera celda dentro de una fila; falso en caso contrario. |
| [IsLastCell](../../aspose.words.tables/cell/islastcell) { get; } | Verdadero si esta es la última celda dentro de una fila; falso en caso contrario. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph) { get; } | Obtiene el último párrafo entre los hijos inmediatos. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.tables/cell/nodetype) { get; } | Devoluciones **NodeType.Cell** . |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs) { get; } | Obtiene una colección de párrafos que son hijos inmediatos de la celda. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentRow](../../aspose.words.tables/cell/parentrow) { get; } | Devuelve la fila principal de la celda. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [Tables](../../aspose.words.tables/cell/tables) { get; } | Obtiene una colección de tablas que son elementos secundarios inmediatos de la celda. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reservado para uso del sistema. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum)() | Si el último elemento secundario no es un párrafo, crea y agrega un párrafo vacío. |
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
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

**Célula** solo puede ser hijo de **Fila**.

**Célula** puede contener nodos a nivel de bloque **Párrafo** y **Mesa**.

Una celda válida mínima debe tener al menos una **Párrafo**.

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
