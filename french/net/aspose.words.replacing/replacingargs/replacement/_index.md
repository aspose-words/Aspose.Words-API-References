---
title: ReplacingArgs.Replacement
second_title: Référence de l'API Aspose.Words pour .NET
description: ReplacingArgs propriété. Obtient ou définit la chaîne de remplacement.
type: docs
weight: 60
url: /fr/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

Obtient ou définit la chaîne de remplacement.

```csharp
public string Replacement { get; set; }
```

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

### Voir également

* class [ReplacingArgs](../)
* espace de noms [Aspose.Words.Replacing](../../replacingargs/)
* Assemblée [Aspose.Words](../../../)


