---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.NodeType pour identifier et gérer facilement différents types de nœuds de documents Word pour un traitement transparent des documents.
type: docs
weight: 4920
url: /fr/net/aspose.words/nodetype/
---
## NodeType enumeration

Spécifie le type d'un nœud de document Word.

```csharp
public enum NodeType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Any | `0` | Indique tous les types de nœuds. Permet de sélectionner tous les enfants. |
| Document | `1` | UN[`Document`](../document/) objet qui, en tant que racine de l'arborescence du document, donne accès à l'ensemble du document Word. |
| Section | `2` | UN[`Section`](../section/) objet qui correspond à une section dans un document Word. |
| Body | `3` | UN[`Body`](../body/) objet qui contient le texte principal d'une section (texte principal de l'histoire). |
| HeaderFooter | `4` | UN[`HeaderFooter`](../headerfooter/) objet qui contient le texte d'un en-tête ou d'un pied de page particulier à l'intérieur d'une section. |
| Table | `5` | UN[`Table`](../../aspose.words.tables/table/) objet qui représente un tableau dans un document Word. |
| Row | `6` | Une rangée d'une table. |
| Cell | `7` | Une cellule d'une ligne de tableau. |
| Paragraph | `8` | Un paragraphe de texte. |
| BookmarkStart | `9` | Un début de marque-page. |
| BookmarkEnd | `10` | Une extrémité d'un marqueur de signet. |
| EditableRangeStart | `11` | Un début de gamme modifiable. |
| EditableRangeEnd | `12` | Une fin d'une plage modifiable. |
| MoveFromRangeStart | `13` | Un début d'une plage MoveFrom. |
| MoveFromRangeEnd | `14` | Une fin d'une plage MoveFrom. |
| MoveToRangeStart | `15` | Un début d'une gamme MoveTo. |
| MoveToRangeEnd | `16` | Une fin d'une plage MoveTo. |
| GroupShape | `17` | Un groupe de formes, d’images, d’objets OLE ou d’autres formes de groupe. |
| Shape | `18` | Un objet de dessin, tel qu'une forme OfficeArt, une image ou un objet OLE. |
| Comment | `19` | Un commentaire dans un document Word. |
| Footnote | `20` | Une note de bas de page ou de fin dans un document Word. |
| Run | `21` | Une série de textes. |
| FieldStart | `22` | Un caractère spécial qui désigne le début d'un champ Word. |
| FieldSeparator | `23` | Un caractère spécial qui sépare le code du champ du résultat du champ. |
| FieldEnd | `24` | Un caractère spécial qui désigne la fin d'un champ Word. |
| FormField | `25` | Un champ de formulaire. |
| SpecialChar | `26` | Un caractère spécial qui ne fait pas partie des types de caractères spéciaux les plus spécifiques. |
| SmartTag | `27` | Une balise intelligente autour d'une ou plusieurs structures en ligne (exécutions, images, champs, etc.) dans un paragraphe |
| StructuredDocumentTag | `28` | Permet de définir des informations spécifiques au client et leurs moyens de présentation. |
| StructuredDocumentTagRangeStart | `29` | Un début de**à distance** balise de document structurée qui accepte un contenu multi-sections. |
| StructuredDocumentTagRangeEnd | `30` | Une fin de**à distance** balise de document structurée qui accepte un contenu multi-sections. |
| GlossaryDocument | `31` | Un document glossaire dans le document principal. |
| BuildingBlock | `32` | Un élément de base dans un document de glossaire (par exemple, une entrée de document de glossaire). |
| CommentRangeStart | `33` | Un nœud marqueur qui représente le début d'une plage commentée. |
| CommentRangeEnd | `34` | Un nœud marqueur qui représente la fin d'une plage commentée. |
| OfficeMath | `35` | Un objet Office Math. Il peut s'agir d'une équation, d'une fonction, d'une matrice ou d'un autre objet mathématique. Il peut s'agir d'une collection d'objets mathématiques et contenir des objets non mathématiques, tels que des séquences de texte. |
| SubDocument | `36` | Un nœud de sous-document qui est un lien vers un autre document. |
| System | `37` | Réservé à un usage interne par Aspose.Words. |
| Null | `38` | Réservé à un usage interne par Aspose.Words. |

## Exemples

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
