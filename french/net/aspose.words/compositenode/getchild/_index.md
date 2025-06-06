---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words pour .NET
description: Découvrez la méthode CompositeNode GetChild pour récupérer facilement le Nième nœud enfant d'un type spécifique, améliorant ainsi l'efficacité de votre gestion des données.
type: docs
weight: 100
url: /fr/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Renvoie un Nième nœud enfant qui correspond au type spécifié.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| nodeType | NodeType | Spécifie le type du nœud enfant. |
| index | Int32 | Index basé sur zéro du nœud enfant à sélectionner. Les index négatifs sont également autorisés et indiquent l'accès depuis la fin, c'est-à-dire -1 signifie le dernier nœud. |
| isDeep | Boolean | `vrai` pour sélectionner parmi tous les nœuds enfants de manière récursive ; `FAUX` Pour sélectionner uniquement parmi les enfants immédiats. Voir les remarques pour plus d'informations. |

### Return_Value

Le nœud enfant qui correspond aux critères ou`nul` si aucun nœud correspondant n'est trouvé.

## Remarques

Si l'index est hors de portée, un`nul` est retourné.

Notez que les nœuds de balisage (StructuredDocumentTag etSmartTag ) sont parcourus même lorsque*isDeep* =`FAUX` et`GetChild` est invoqué pour un type de nœud non balisé. Par exemple, si la première exécution d'un paramètre para est encapsulée dans un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , il sera toujours retourné par`GetChild`(Run , 0,`FAUX`).

## Exemples

Montre comment appliquer les propriétés du style d'un tableau directement aux éléments du tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Cette méthode concerne les propriétés de style de tableau telles que celles que nous avons définies ci-dessus.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Montre comment parcourir la collection de nœuds enfants d'un nœud composite.

```csharp
Document doc = new Document();

// Ajoutez deux exécutions et une forme en tant que nœuds enfants au premier paragraphe de ce document.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Notez que le « CustomNodeId » n'est pas enregistré dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Parcourir la collection d'enfants immédiats du paragraphe,
// et imprimez toutes les séquences ou formes que nous trouvons à l'intérieur.
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

### Voir également

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
