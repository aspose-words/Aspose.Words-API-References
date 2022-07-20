---
title: GetAncestor
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient le premier ancêtre du type dobjet spécifié.
type: docs
weight: 110
url: /fr/net/aspose.words/node/getancestor/
---
## GetAncestor(Type) {#getancestor_1}

Obtient le premier ancêtre du type d'objet spécifié.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| ancestorType | Type | Le type d'objet de l'ancêtre à récupérer. |

### Return_Value

L'ancêtre du type spécifié ou null si aucun ancêtre de ce type n'a été trouvé.

### Remarques

Le type d'ancêtre correspond s'il est égal à ancestorType ou dérivé de ancestorType.

### Exemples

Montre comment savoir si une table est imbriquée.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);

    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Détermine si des cellules du tableau ont d'autres tableaux comme enfants.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Détermine si la table est imbriquée dans une autre table et, si oui, à quelle profondeur.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcule à quel niveau une table est imbriquée dans d'autres tables.
/// </summary>
/// <returns>
/// Un entier indiquant la profondeur d'imbrication de la table (nombre de nœuds de la table parent).
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
/// Détermine si une table contient une table enfant immédiate dans ses cellules.
/// Ne parcourez pas ces tables de manière récursive pour rechercher d'autres tables.
/// </summary>
/// <returns>
/// Renvoie true si au moins une cellule enfant contient un tableau.
/// Renvoie faux si aucune cellule du tableau ne contient de tableau.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows.OfType<Row>())
    {
        foreach (Cell Cell in row.Cells.OfType<Cell>())
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### Voir également

* class [CompositeNode](../../compositenode)
* class [Node](../../node)
* espace de noms [Aspose.Words](../../node)
* Assemblée [Aspose.Words](../../../)

---

## GetAncestor(NodeType) {#getancestor}

Obtient le premier ancêtre du spécifié[`NodeType`](../../nodetype) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| ancestorType | NodeType | Type de nœud de l'ancêtre à récupérer. |

### Return_Value

L'ancêtre du type spécifié ou null si aucun ancêtre de ce type n'a été trouvé.

### Exemples

Montre comment savoir si une table est imbriquée.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);

    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Détermine si des cellules du tableau ont d'autres tableaux comme enfants.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Détermine si la table est imbriquée dans une autre table et, si oui, à quelle profondeur.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcule à quel niveau une table est imbriquée dans d'autres tables.
/// </summary>
/// <returns>
/// Un entier indiquant la profondeur d'imbrication de la table (nombre de nœuds de la table parent).
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
/// Détermine si une table contient une table enfant immédiate dans ses cellules.
/// Ne parcourez pas ces tables de manière récursive pour rechercher d'autres tables.
/// </summary>
/// <returns>
/// Renvoie true si au moins une cellule enfant contient un tableau.
/// Renvoie faux si aucune cellule du tableau ne contient de tableau.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows.OfType<Row>())
    {
        foreach (Cell Cell in row.Cells.OfType<Cell>())
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### Voir également

* class [CompositeNode](../../compositenode)
* enum [NodeType](../../nodetype)
* class [Node](../../node)
* espace de noms [Aspose.Words](../../node)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
