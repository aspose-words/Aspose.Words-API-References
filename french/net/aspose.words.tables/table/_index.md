---
title: Class Table
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Tables.Table classe. Représente un tableau dans un document Word.
type: docs
weight: 6040
url: /fr/net/aspose.words.tables/table/
---
## Table class

Représente un tableau dans un document Word.

```csharp
public class Table : CompositeNode
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [Table](table/)(DocumentBase) | Initialise une nouvelle instance du **Table** classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Obtient ou définit la position horizontale absolue du tableau flottant spécifiée par les propriétés du tableau, en points. La valeur par défaut est 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Obtient ou définit la position verticale absolue du tableau flottant spécifiée par les propriétés du tableau, en points. La valeur par défaut est 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Spécifie comment un tableau en ligne est aligné dans le document. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Permet à Microsoft Word et Aspose.Words de redimensionner automatiquement les cellules d'un tableau en fonction de leur contenu. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Obtient ou définit l'option "Autoriser l'espacement entre les cellules". |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Obtient si une table flottante doit autoriser d'autres objets flottants dans le document à chevaucher ses étendues lorsqu'il est affiché. La valeur par défaut est`vrai` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Obtient ou définit s'il s'agit d'un tableau de droite à gauche. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Obtient ou définit la quantité d'espace (en points) entre les cellules. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtient tous les nœuds enfants immédiats de ce nœud. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtient le nombre d'enfants immédiats de ce nœud. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Obtient ou définit la description de ce tableau. Il fournit une représentation textuelle alternative des informations contenues dans le tableau. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; } | Obtient la distance entre le bas du tableau et le texte environnant, en points. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; } | Obtient la distance entre le tableau à gauche et le texte environnant, en points. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; } | Obtient la distance entre la droite du tableau et le texte environnant, en points. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; } | Obtient la distance entre le dessus du tableau et le texte environnant, en points. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtient le premier enfant du nœud. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Renvoie le premier **Ligne** nœud dans la table. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Renvoie vrai si ce nœud a des nœuds enfants. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Obtient l'objet de base à partir duquel le positionnement horizontal du tableau flottant doit être calculé. La valeur par défaut estColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Renvoie true car ce nœud peut avoir des nœuds enfants. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtient le dernier enfant du nœud. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Renvoie le dernier **Ligne** nœud dans la table. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Obtient ou définit la valeur qui représente le retrait à gauche du tableau. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | Retours **NodeType.Table** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Obtient ou définit la largeur préférée du tableau. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Obtient ou définit l'alignement horizontal relatif du tableau flottant. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Obtient ou définit l'alignement vertical relatif de la table flottante. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Fournit un accès typé aux lignes de la table. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Obtient ou définit le style de tableau appliqué à ce tableau. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Obtient ou définit l'identificateur de style indépendant des paramètres régionaux du style de table appliqué à cette table. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Obtient ou définit le nom du style de tableau appliqué à ce tableau. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Obtient ou définit des indicateurs binaires qui spécifient comment un style de tableau est appliqué à ce tableau. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Obtient ou définit[`TextWrapping`](./textwrapping/) pour le tableau. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Obtient ou définit le titre de cette table. Il fournit une représentation textuelle alternative des informations contenues dans la table. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Obtient l'objet de base à partir duquel le positionnement vertical du tableau flottant doit être calculé. La valeur par défaut estMargin . |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Ajoute le nœud spécifié à la fin de la liste des nœuds enfants pour ce nœud. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(AutoFitBehavior) | Redimensionne le tableau et les cellules en fonction du comportement d'ajustement automatique spécifié. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Supprime toutes les bordures de tableau et de cellule de ce tableau. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Supprime tous les ombrages du tableau. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées par[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Réservé à l'utilisation du système. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Si le tableau n'a pas de lignes, en crée et en ajoute une **Ligne** . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Renvoie un Nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Renvoie l'index du nœud enfant spécifié dans le tableau de nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Insère le nœud spécifié immédiatement après le nœud de référence spécifié. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Insère le nœud spécifié juste avant le nœud de référence spécifié. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Ajoute le nœud spécifié au début de la liste des nœuds enfants pour ce nœud. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Supprime le nœud enfant spécifié. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tout[`SmartTag`](../../aspose.words.markup/smarttag/) nœuds descendants du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Sélectionne le premier nœud qui correspond à l'expression XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(BorderType, LineStyle, double, Color, bool) | Définit la bordure de tableau spécifiée sur le style de ligne, la largeur et la couleur spécifiés. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(LineStyle, double, Color) | Définit toutes les bordures de tableau sur le style de ligne, la largeur et la couleur spécifiés. |
| [SetShading](../../aspose.words.tables/table/setshading/)(TextureIndex, Color, Color) | Définit l'ombrage aux valeurs spécifiées sur l'ensemble du tableau. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

**Table**est un nœud de niveau bloc et peut être un enfant de classes dérivées de **Histoire** ou  **InlineStory**.

**Table** peut contenir un ou plusieurs **Ligne** nœuds.

Une table minimale valide doit avoir au moins un **Ligne**.

### Exemples

Montre comment créer une table.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Les tableaux contiennent des lignes, qui contiennent des cellules, qui peuvent avoir des paragraphes
// avec des éléments typiques tels que des suites, des formes et même d'autres tables.
// L'appel de la méthode "EnsureMinimum" sur une table garantira que
// le tableau contient au moins une ligne, une cellule et un paragraphe.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Ajoute du texte au premier appel dans la première ligne du tableau.
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

    // Nous pouvons utiliser la méthode "ToArray" sur une collection de lignes pour la cloner dans un tableau.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Nous pouvons utiliser la méthode "ToArray" sur une collection de cellules pour la cloner dans un tableau.
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

Montre comment créer un tableau 2x2 formaté.

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

// Les lignes et les cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications apportées à la mise en forme du générateur.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Montre comment créer un tableau imbriqué sans utiliser de générateur de document.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Crée le tableau externe avec trois lignes et quatre colonnes, puis l'ajoute au document.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Crée un autre tableau avec deux lignes et deux colonnes, puis insère-le dans la première cellule du premier tableau.
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

    // Vous pouvez utiliser les propriétés "Titre" et "Description" pour ajouter respectivement un titre et une description à votre tableau.
    // La table doit avoir au moins une ligne avant que nous puissions utiliser ces propriétés.
    // Ces propriétés sont significatives pour les documents .docx conformes à la norme ISO/IEC 29500 (voir la classe OoxmlCompliance).
    // Si nous enregistrons le document dans des formats pré-ISO/IEC 29500, Microsoft Word ignore ces propriétés.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Voir également

* class [CompositeNode](../../aspose.words/compositenode/)
* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)


