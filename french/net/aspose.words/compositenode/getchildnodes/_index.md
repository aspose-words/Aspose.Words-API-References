---
title: GetChildNodes
second_title: Référence de l'API Aspose.Words pour .NET
description: Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié.
type: docs
weight: 100
url: /fr/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Renvoie une collection dynamique de nœuds enfants correspondant au type spécifié.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| nodeType | NodeType | Spécifie le type de nœuds à sélectionner. |
| isDeep | Boolean | True pour sélectionner parmi tous les nœuds enfants de manière récursive. False pour sélectionner uniquement parmi les enfants immédiats. |

### Return_Value

Une collection active de nœuds enfants du type spécifié.

### Remarques

La collection de nœuds renvoyée par cette méthode est toujours active.

Une collection dynamique est toujours synchronisée avec le document. Par exemple, si vous avez sélectionné toutes les sections d'un document et que vous avez énuméré la collection en supprimant les sections, la section est supprimée de la collection immédiatement lorsqu'elle est supprimée du document.

### Exemples

Montre comment imprimer tous les commentaires d'un document et leurs réponses.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Si un commentaire n'a pas d'ancêtre, il s'agit d'un commentaire "de niveau supérieur" par opposition à un commentaire de type réponse.
// Affiche tous les commentaires de haut niveau avec toutes les réponses qu'ils peuvent avoir.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

Montre comment extraire des images d'un document et les enregistrer dans le système de fichiers local en tant que fichiers individuels.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Récupère la collection de formes du document,
// et enregistrez les données d'image de chaque forme avec une image en tant que fichier dans le système de fichiers local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Les données d'image des formes peuvent contenir des images de nombreux formats d'image possibles. 
        // Nous pouvons déterminer automatiquement une extension de fichier pour chaque image, en fonction de son format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Montre comment ajouter, mettre à jour et supprimer des nœuds enfants dans la collection d'enfants d'un CompositeNode.

```csharp
Document doc = new Document();

// Un document vide, par défaut, a un paragraphe.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Les nœuds composites tels que notre paragraphe peuvent contenir d'autres nœuds composites et en ligne comme enfants.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crée trois nœuds d'exécution supplémentaires.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Le corps du document n'affichera pas ces passages tant que nous ne les aurons pas insérés dans un nœud composite
// qui lui-même fait partie de l'arborescence des nœuds du document, comme nous l'avons fait lors de la première exécution.
// Nous pouvons déterminer où le contenu textuel des nœuds que nous insérons
// apparaît dans le document en spécifiant un emplacement d'insertion par rapport à un autre nœud du paragraphe.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Insère la deuxième séquence dans le paragraphe devant la séquence initiale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Insère la troisième exécution après l'exécution initiale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Insère la première séquence au début de la collection de nœuds enfants du paragraphe.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Nous pouvons modifier le contenu de l'exécution en modifiant et en supprimant les nœuds enfants existants.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Voir également

* class [NodeCollection](../../nodecollection/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../compositenode/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
