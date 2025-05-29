---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Tables.Table pour créer et gérer facilement des tableaux dans des documents Word, améliorant ainsi la mise en page et les fonctionnalités de votre document.
type: docs
weight: 7190
url: /fr/net/aspose.words.tables/table/
---
## Table class

Représente un tableau dans un document Word.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article de documentation.

```csharp
public class Table : CompositeNode
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initialise une nouvelle instance du`Table` classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Obtient ou définit la position horizontale absolue du tableau flottant spécifiée par les propriétés du tableau, en points. La valeur par défaut est 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Obtient ou définit la position verticale absolue du tableau flottant spécifiée par les propriétés du tableau, en points. La valeur par défaut est 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Spécifie comment un tableau en ligne est aligné dans le document. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Permet à Microsoft Word et Aspose.Words de redimensionner automatiquement les cellules d'un tableau pour les adapter à leur contenu. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Obtient ou définit l'option « Autoriser l'espacement entre les cellules ». |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Détermine si une table flottante doit autoriser d'autres objets flottants dans le document à chevaucher ses étendues lorsqu'ils sont affichés. La valeur par défaut est`vrai` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Obtient ou définit s'il s'agit d'un tableau de droite à gauche. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Obtient ou définit la quantité d'espace (en points) entre les cellules. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Obtient ou définit la description de cette table. Il fournit une représentation textuelle alternative des informations contenues dans la table. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Obtient ou définit la distance entre le bas du tableau et le texte environnant, en points. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Obtient ou définit la distance entre la gauche du tableau et le texte environnant, en points. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Obtient ou définit la distance entre la droite du tableau et le texte environnant, en points. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Obtient ou définit la distance entre le dessus de la table et le texte environnant, en points. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Renvoie le premier[`Row`](../row/) nœud dans la table. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Retours`vrai` si ce nœud a des nœuds enfants. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Obtient l'objet de base à partir duquel le positionnement horizontal du tableau flottant doit être calculé. La valeur par défaut estColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Retours`vrai` car ce nœud peut avoir des nœuds enfants. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Renvoie le dernier[`Row`](../row/) nœud dans la table. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Obtient ou définit la valeur qui représente le retrait à gauche du tableau. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | RetoursTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Obtient ou définit la largeur préférée du tableau. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/)objet qui représente la partie d'un document contenue dans ce nœud. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Obtient ou définit l'alignement horizontal relatif de la table flottante. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Obtient ou définit l'alignement vertical relatif de la table flottante. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Fournit un accès typé aux lignes de la table. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Obtient ou définit le style de tableau appliqué à ce tableau. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Obtient ou définit l'identifiant de style indépendant des paramètres régionaux du style de table appliqué à cette table. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Obtient ou définit le nom du style de tableau appliqué à ce tableau. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Obtient ou définit des indicateurs binaires qui spécifient comment un style de tableau est appliqué à ce tableau. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Obtient ou définit[`TextWrapping`](./textwrapping/) pour la table. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Obtient ou définit le titre de ce tableau. Il fournit une représentation textuelle alternative des informations contenues dans le tableau. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Obtient l'objet de base à partir duquel le positionnement vertical du tableau flottant doit être calculé. La valeur par défaut estMargin . |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter la fin de la table. |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur pour visiter le début de la table. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Redimensionne le tableau et les cellules en fonction du comportement d'ajustement automatique spécifié. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Supprime toutes les bordures de tableau et de cellule de ce tableau. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Supprime tout l'ombrage sur le tableau. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées par[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crée un navigateur qui peut être utilisé pour parcourir et lire les nœuds. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Si la table ne contient aucune ligne, crée et ajoute une ligne[`Row`](../row/) . |
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
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Définit la bordure de tableau spécifiée sur le style de ligne, la largeur et la couleur spécifiés. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Définit toutes les bordures du tableau selon le style de ligne, la largeur et la couleur spécifiés. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Définit l'ombrage sur les valeurs spécifiées sur l'ensemble du tableau. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |

## Remarques

`Table` est un nœud de niveau bloc et peut être un enfant de classes dérivées de[`Story`](../../aspose.words/story/) ou [`InlineStory`](../../aspose.words/inlinestory/).

`Table` peut contenir un ou plusieurs[`Row`](../row/) nœuds.

Une table minimale valide doit avoir au moins un[`Row`](../row/).

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

Montre comment créer un tableau formaté 2x2.

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

// Lors de la construction du tableau, le générateur de documents appliquera ses valeurs de propriété RowFormat/CellFormat actuelles
// à la ligne/cellule actuelle dans laquelle se trouve son curseur et à toutes les nouvelles lignes/cellules au fur et à mesure qu'il les crée.
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

// Les lignes et cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications apportées à la mise en forme du générateur.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
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
