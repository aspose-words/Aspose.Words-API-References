---
title: Enum NodeType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.NodeType énumération. Spécifie le type dun nœud de document Word.
type: docs
weight: 4230
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
| Document | `1` | UN[`Document`](../document/) objet qui, en tant que racine de l'arborescence du document, donne accès à l'intégralité du document Word. |
| Section | `2` | UN[`Section`](../section/) objet qui correspond à une section d’un document Word. |
| Body | `3` | UN[`Body`](../body/) objet qui contient le texte principal d'une section (histoire du texte principal). |
| HeaderFooter | `4` | UN[`HeaderFooter`](../headerfooter/) objet qui contient le texte d’un en-tête ou d’un pied de page particulier à l’intérieur d’une section. |
| Table | `5` | UN[`Table`](../../aspose.words.tables/table/) objet qui représente un tableau dans un document Word. |
| Row | `6` | Une rangée d'un tableau. |
| Cell | `7` | Cellule d'une ligne de tableau. |
| Paragraph | `8` | Un paragraphe de texte. |
| BookmarkStart | `9` | Un début de marque-page. |
| BookmarkEnd | `10` | Une fin d’un marqueur de signet. |
| EditableRangeStart | `11` | Un début d’une plage modifiable. |
| EditableRangeEnd | `12` | Fin d'une plage modifiable. |
| MoveFromRangeStart | `13` | Début d’une plage MoveFrom. |
| MoveFromRangeEnd | `14` | Fin d’une plage MoveFrom. |
| MoveToRangeStart | `15` | Un début d’une plage MoveTo. |
| MoveToRangeEnd | `16` | Fin d’une plage MoveTo. |
| GroupShape | `17` | Un groupe de formes, d'images, d'objets OLE ou d'autres formes de groupe. |
| Shape | `18` | Un objet de dessin, tel qu'une forme OfficeArt, une image ou un objet OLE. |
| Comment | `19` | Un commentaire dans un document Word. |
| Footnote | `20` | Une note de bas de page ou une note de fin dans un document Word. |
| Run | `21` | Une suite de texte. |
| FieldStart | `22` | Caractère spécial qui désigne le début d'un champ Word. |
| FieldSeparator | `23` | Caractère spécial qui sépare le code du champ du résultat du champ. |
| FieldEnd | `24` | Caractère spécial qui désigne la fin d'un champ Word. |
| FormField | `25` | Un champ de formulaire. |
| SpecialChar | `26` | Caractère spécial qui ne fait pas partie des types de caractères spéciaux les plus spécifiques. |
| SmartTag | `27` | Une balise active autour d'une ou plusieurs structures en ligne (exécutions, images, champs, etc.) dans un paragraphe |
| StructuredDocumentTag | `28` | Permet de définir les informations spécifiques au client et ses modalités de présentation. |
| StructuredDocumentTagRangeStart | `29` | Un début de **à distance** balise de document structuré qui accepte le contenu multi-sections. |
| StructuredDocumentTagRangeEnd | `30` | Une fin de **à distance** balise de document structuré qui accepte le contenu multi-sections. |
| GlossaryDocument | `31` | Un document glossaire dans le document principal. |
| BuildingBlock | `32` | Un élément de base dans un document de glossaire (par exemple, entrée de document de glossaire). |
| CommentRangeStart | `33` | Un nœud marqueur qui représente le début d'une plage commentée. |
| CommentRangeEnd | `34` | Un nœud marqueur qui représente la fin d'une plage commentée. |
| OfficeMath | `35` | Un objet Office Math. Peut être une équation, une fonction, une matrice ou l'un des autres objets mathématiques. Peut être une collection d'objets mathématiques et peut également contenir des objets non mathématiques tels que des séquences de texte. |
| SubDocument | `36` | Un nœud de sous-document qui est un lien vers un autre document. |
| System | `37` | Réservé à un usage interne par Aspose.Words. |
| Null | `38` | Réservé à un usage interne par Aspose.Words. |

### Exemples

Montre comment parcourir la collection de nœuds enfants d’un nœud composite.

```csharp
Document doc = new Document();

// Ajoutez deux tracés et une forme en tant que nœuds enfants au premier paragraphe de ce document.
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

// Parcourir la collection d'enfants immédiats du paragraphe,
// et imprimons toutes les courses ou formes que nous trouvons à l'intérieur.
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


