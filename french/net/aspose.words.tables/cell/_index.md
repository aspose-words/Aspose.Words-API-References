---
title: Cell Class
linktitle: Cell
articleTitle: Cell
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Tables.Cell  votre solution pour une gestion efficace des cellules de tableau dans le traitement de vos documents. Améliorez votre flux de travail dès aujourd'hui !
type: docs
weight: 7090
url: /fr/net/aspose.words.tables/cell/
---
## Cell class

Représente une cellule de tableau.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article de documentation.

```csharp
public class Cell : CompositeNode
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Cell](cell/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initialise une nouvelle instance du`Cell` classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat/) { get; } | Donne accès aux propriétés de formatage de la cellule. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph/) { get; } | Obtient le premier paragraphe parmi les enfants immédiats. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell/) { get; } | Vrai s'il s'agit de la première cellule d'une ligne ; faux sinon. |
| [IsLastCell](../../aspose.words.tables/cell/islastcell/) { get; } | Vrai s'il s'agit de la dernière cellule d'une ligne ; faux sinon. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph/) { get; } | Obtient le dernier paragraphe parmi les enfants immédiats. |
| [NextCell](../../aspose.words.tables/cell/nextcell/) { get; } | Obtient le suivant`Cell` nœud. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.tables/cell/nodetype/) { get; } | RetoursCell . |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs/) { get; } | Obtient une collection de paragraphes qui sont les enfants immédiats de la cellule. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentRow](../../aspose.words.tables/cell/parentrow/) { get; } | Renvoie la ligne parent de la cellule. |
| [PreviousCell](../../aspose.words.tables/cell/previouscell/) { get; } | Obtient le précédent`Cell` nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [Tables](../../aspose.words.tables/cell/tables/) { get; } | Obtient une collection de tables qui sont les enfants immédiats de la cellule. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words.tables/cell/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter la fin de la cellule. |
| override [AcceptStart](../../aspose.words.tables/cell/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter le début de la cellule. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire les nœuds. |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum/)() | Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit un support pour chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Insère le nœud spécifié immédiatement avant le nœud de référence spécifié. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Sélectionne le premier[`Node`](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |

## Remarques

`Cell` ne peut être qu'un enfant d'un[`Row`](../row/).

`Cell` peut contenir des nœuds au niveau du bloc[`Paragraph`](../../aspose.words/paragraph/) et[`Table`](../table/).

Une cellule minimale valide doit avoir au moins un[`Paragraph`](../../aspose.words/paragraph/).

## Exemples

Montre comment créer un tableau.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Les tableaux contiennent des lignes, qui contiennent des cellules, qui peuvent contenir des paragraphes
// avec des éléments typiques tels que des exécutions, des formes et même d'autres tables.
// L'appel de la méthode « EnsureMinimum » sur une table garantira que
// le tableau comporte au moins une ligne, une cellule et un paragraphe.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Ajoutez du texte à la première cellule de la première ligne du tableau.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Montre comment parcourir tous les tableaux du document et imprimer le contenu de chaque cellule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Nous pouvons utiliser la méthode « ToArray » sur une collection de lignes pour la cloner dans un tableau.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Nous pouvons utiliser la méthode « ToArray » sur une collection de cellules pour la cloner dans un tableau.
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

Montre comment créer un tableau imbriqué sans utiliser de générateur de documents.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Créez le tableau externe avec trois lignes et quatre colonnes, puis ajoutez-le au document.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Créez un autre tableau avec deux lignes et deux colonnes, puis insérez-le dans la première cellule du premier tableau.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crée un nouveau tableau dans le document avec les dimensions et le texte donnés dans chaque cellule.
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

    // Vous pouvez utiliser les propriétés « Titre » et « Description » pour ajouter respectivement un titre et une description à votre tableau.
    // La table doit avoir au moins une ligne avant que nous puissions utiliser ces propriétés.
    // Ces propriétés sont significatives pour les documents .docx conformes à la norme ISO / IEC 29500 (voir la classe OoxmlCompliance).
    // Si nous enregistrons le document dans des formats antérieurs à ISO/IEC 29500, Microsoft Word ignore ces propriétés.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Voir également

* class [CompositeNode](../../aspose.words/compositenode/)
* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
