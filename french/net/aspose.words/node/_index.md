---
title: Class Node
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Node classe. Classe de base pour tous les nœuds dun document Word.
type: docs
weight: 3930
url: /fr/net/aspose.words/node/
---
## Node class

Classe de base pour tous les nœuds d'un document Word.

```csharp
public abstract class Node
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtient le type de ce nœud. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor_1)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring/#tostring_1)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/#tostring_2)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(NodeType) | Une méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |

### Remarques

Un document est représenté comme une arborescence de nœuds, similaire à DOM ou XmlDocument.

Pour plus d'informations, consultez le modèle de conception Composite.

La`Node`classer:

* Définit l'interface du nœud enfant.
* Définit l'interface pour visiter les nœuds.
* Fournit une capacité de clonage par défaut.
* Implémente les mécanismes de nœud parent et de document propriétaire.
* Implémente l'accès aux nœuds frères.

### Exemples

Montre comment supprimer tous les nœuds enfants d'un type spécifique d'un nœud composite.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Enregistre le nœud frère suivant en tant que variable au cas où nous voudrions y accéder après avoir supprimé ce nœud.
    Node nextNode = curNode.NextSibling;

    // Un corps de section peut contenir des nœuds Paragraphe et Table.
    // Si le nœud est une table, supprimez-le du parent.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

Montre comment cloner un nœud composite.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Vous trouverez ci-dessous deux manières de cloner un nœud composite.
// 1 - Crée un clone d'un nœud et crée également un clone de chacun de ses nœuds enfants.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Créer un clone d'un nœud tout seul sans aucun enfant.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

Montre comment parcourir la collection de nœuds enfants d'un nœud composite.

```csharp
Document doc = new Document();

// Ajoutez deux passages et une forme en tant que nœuds enfants au premier paragraphe de ce document.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Notez que le 'CustomNodeId' n'est pas enregistré dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Parcourt la collection d'enfants immédiats du paragraphe,
// et imprimez toutes les pistes ou formes que nous trouvons à l'intérieur.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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
    }
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


