---
title: NodeCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà NodeCollection Count per accedere facilmente al numero totale di nodi nella tua raccolta, migliorando l'efficienza e la gestione dei dati.
type: docs
weight: 10
url: /it/net/aspose.words/nodecollection/count/
---
## NodeCollection.Count property

Ottiene il numero di nodi nella raccolta.

```csharp
public int Count { get; }
```

## Esempi

Mostra come attraversare la raccolta di nodi figlio di un nodo composito.

```csharp
Document doc = new Document();

// Aggiungere due sequenze e una forma come nodi figlio al primo paragrafo di questo documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Nota che 'CustomNodeId' non viene salvato in un file di output ed esiste solo per la durata del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Scorrere la raccolta di elementi figlio immediati del paragrafo,
// e stampare tutte le sequenze o le forme che troviamo al suo interno.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

Mostra come scoprire se le tabelle sono annidate.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Scopri se ci sono celle nella tabella che hanno altre tabelle come figlie.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Scopri se la tabella è annidata all'interno di un'altra tabella e, in tal caso, a quale profondità.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcola a quale livello una tabella è annidata all'interno di altre tabelle.
/// </summary>
/// <returns>
/// Un numero intero che indica la profondità di annidamento della tabella (numero di nodi della tabella padre).
/// </returns>
private static int GetNestedDepthOfTable(Table table)
{
    int depth = 0;
    Node parent = table.GetAncestor(table.NodeType);

    while (parent != null)
    {
        depth++;
        parent = parent.GetAncestor(typeof(Table));
    }

    return depth;
}

/// <summary>
/// Determina se una tabella contiene una tabella figlia immediata all'interno delle sue celle.
/// Non attraversare ricorsivamente queste tabelle per controllare altre tabelle.
/// </summary>
/// <returns>
/// Restituisce true se almeno una cella figlia contiene una tabella.
/// Restituisce false se nessuna cella nella tabella contiene una tabella.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows)
    {
        foreach (Cell Cell in row.Cells)
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### Guarda anche

* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
