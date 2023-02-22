---
title: Class NodeCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.NodeCollection classe. Représente une collection de nœuds dun type spécifique.
type: docs
weight: 3960
url: /fr/net/aspose.words/nodecollection/
---
## NodeCollection class

Représente une collection de nœuds d'un type spécifique.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Récupère un nœud à l'index donné. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Détermine si un nœud est dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une simple itération de style "foreach" sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copie tous les nœuds de la collection vers un nouveau tableau de nœuds. |

### Remarques

**NodeCollection** ne possède pas les nœuds qu'il contient, est plutôt une sélection de nodes du type spécifié, mais les nœuds sont stockés dans l'arborescence sous leurs nœuds parents respectifs.

**NodeCollection**prend en charge l'accès indexé, l'itération et fournit des méthodes d'ajout et de suppression.

La **NodeCollection** la collection est "en direct", c'est-à-dire que les modifications apportées aux enfants du nœud object à partir duquel elle a été créée sont immédiatement reflétées dans les nœuds renvoyés par le **NodeCollection** propriétés et méthodes.

**NodeCollection** est renvoyé par[`GetChildNodes`](../compositenode/getchildnodes/) et sert également de classe de base pour les collections de nœuds typés telles que[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) etc.

**NodeCollection** peut être "plat" et contenir uniquement les enfants immédiats du nœud à partir duquel il a été créé , ou il peut être "profond" et contenir tous les enfants descendants.

### Exemples

Montre comment remplacer toutes les formes de zone de texte par des formes d'image.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Voir également

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


