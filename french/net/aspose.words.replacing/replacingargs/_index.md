---
title: ReplacingArgs
second_title: Référence de l'API Aspose.Words pour .NET
description: Fournit des données pour une opération de remplacement personnalisée.
type: docs
weight: 4390
url: /fr/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Fournit des données pour une opération de remplacement personnalisée.

```csharp
public class ReplacingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex/) { get; set; } | Identifie, par index, un groupe capturé dans la[`Match`](./match/) qui doit être remplacé par le[`Replacement`](./replacement/) chaîne. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname/) { get; set; } | Identifie, par son nom, un groupe capturé dans le[`Match`](./match/) qui doit être remplacé par le[`Replacement`](./replacement/) chaîne. |
| [Match](../../aspose.words.replacing/replacingargs/match/) { get; } | LeMatch résultant d'une seule correspondance d'expression regular lors d'une **Remplacer** . |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode/) { get; } | Obtient le nœud qui contient le début de la correspondance. |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset/) { get; } | Obtient la position de départ à base zéro de la correspondance à partir du début de le nœud qui contient le début de la correspondance. |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement/) { get; set; } | Obtient ou définit la chaîne de remplacement. |

### Exemples

Montre comment remplacer toutes les occurrences d'un modèle d'expression régulière par une autre chaîne, tout en suivant tous ces remplacements.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();

    // Définit un rappel qui suit tous les remplacements que la méthode "Replace" effectuera.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Maintient un journal de chaque remplacement de texte effectué par une opération de recherche et de remplacement
/// et note la valeur du texte correspondant d'origine.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

Montre comment insérer le contenu d'un document entier en remplacement d'une correspondance dans une opération de recherche et de remplacement.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Insère un document après le paragraphe contenant le texte correspondant.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Supprime le paragraphe avec le texte correspondant.
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
                // Ignore le nœud s'il s'agit du dernier paragraphe vide d'une section.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
