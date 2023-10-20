---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words pour .NET
description: NodeImporter ImportNode méthode. Importe un nœud dun document dans un autre en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Importe un nœud d'un document dans un autre.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcNode | Node | Le nœud à importer. |
| isImportChildren | Boolean | `vrai` pour importer tous les nœuds enfants de manière récursive ; sinon,`FAUX`. |

### Return_Value

Le nœud cloné et importé. Le nœud appartient au document de destination, mais n'a pas de parent.

## Remarques

L'importation d'un nœud crée une copie du nœud source appartenant au document importateur. Le nœud renvoyé n'a pas de parent. Le nœud source n'est ni modifié ni supprimé du document d'origine.

Avant qu'un nœud d'un autre document puisse être inséré dans ce document, il doit être importé. Lors de l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Une fois le nœud importé, il peut être inséré à l'endroit approprié dans le document en utilisant[`InsertBefore`](../../compositenode/insertbefore/) ou [`InsertAfter`](../../compositenode/insertafter/).

Si le nœud source appartient déjà au document de destination, alors simplement un clone profond du nœud source est créé.

## Exemples

Montre comment insérer le contenu d’un document dans un signet dans un autre document.

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// Insère le contenu d'un document après le nœud spécifié.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Parcourez tous les nœuds de niveau bloc dans le corps de la section,
        // puis clonez et insérez chaque nœud qui n'est pas le dernier paragraphe vide d'une section.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### Voir également

* class [Node](../../node/)
* class [NodeImporter](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
