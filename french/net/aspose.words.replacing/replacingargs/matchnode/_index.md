---
title: ReplacingArgs.MatchNode
linktitle: MatchNode
articleTitle: MatchNode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ReplacingArgs MatchNode pour accéder facilement au nœud où commence votre correspondance, améliorant ainsi l'efficacité et la précision de votre codage.
type: docs
weight: 40
url: /fr/net/aspose.words.replacing/replacingargs/matchnode/
---
## ReplacingArgs.MatchNode property

Obtient le nœud qui contient le début de la correspondance.

```csharp
public Node MatchNode { get; }
```

## Exemples

Montre comment insérer le contenu entier d'un document en remplacement d'une correspondance dans une opération de recherche et de remplacement.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Insérer un document après le paragraphe contenant le texte correspondant.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Supprimez le paragraphe avec le texte correspondant.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Insère tous les nœuds d'un autre document après un paragraphe ou un tableau.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Ignorer le nœud s'il s'agit du dernier paragraphe vide d'une section.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### Voir également

* class [Node](../../../aspose.words/node/)
* class [ReplacingArgs](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
