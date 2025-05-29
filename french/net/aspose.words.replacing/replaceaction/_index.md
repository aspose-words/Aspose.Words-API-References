---
title: ReplaceAction Enum
linktitle: ReplaceAction
articleTitle: ReplaceAction
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.ReplaceAction pour contrôler les résultats de correspondance dans vos opérations de remplacement, améliorant ainsi l'efficacité et la précision de l'édition de documents.
type: docs
weight: 5370
url: /fr/net/aspose.words.replacing/replaceaction/
---
## ReplaceAction enumeration

Permet à l'utilisateur de spécifier ce qui arrive à la correspondance actuelle lors d'une opération de remplacement.

```csharp
public enum ReplaceAction
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Replace | `0` | Remplacez la correspondance actuelle. |
| Skip | `1` | Ignorer le match en cours. |
| Stop | `2` | Terminez l'opération de remplacement. |

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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* espace de noms [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../)
