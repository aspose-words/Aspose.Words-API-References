---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words FindReplaceDirection pour un remplacement de texte efficace. Optimisez le traitement de vos documents grâce à un contrôle précis de la direction.
type: docs
weight: 5340
url: /fr/net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

Spécifie la direction des opérations de remplacement.

```csharp
public enum FindReplaceDirection
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Forward | `0` | Les éléments correspondants sont remplacés du premier au dernier. |
| Backward | `1` | Les éléments correspondants sont remplacés du dernier au premier. |

## Exemples

Montre comment déterminer dans quelle direction une opération de recherche et de remplacement traverse le document.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insérez trois exécutions que nous pouvons rechercher à l'aide d'un modèle regex.
    // Placez l'une de ces exécutions dans une zone de texte.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();

    // Attribuez un rappel personnalisé à la propriété « ReplacingCallback ».
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Définissez la propriété « Direction » sur « FindReplaceDirection.Backward » pour obtenir la fonction de recherche et de remplacement
    // opération pour démarrer à partir de la fin de la plage et revenir au début.
    // Définissez la propriété « Direction » sur « FindReplaceDirection.Forward » pour obtenir la fonction de recherche et de remplacement
    // opération pour démarrer depuis le début de la plage et parcourir jusqu'à la fin.
    options.Direction = findReplaceDirection;

    doc.Range.Replace(new Regex(@"Match \d*"), "Replacement", options);

    Assert.AreEqual("Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.", doc.GetText().Trim());

    switch (findReplaceDirection)
    {
        case FindReplaceDirection.Forward:
            Assert.AreEqual(new[] { "Match 1", "Match 2", "Match 3", "Match 4" }, callback.Matches);
            break;
        case FindReplaceDirection.Backward:
            Assert.AreEqual(new[] { "Match 4", "Match 3", "Match 2", "Match 1" }, callback.Matches);
            break;
    }
}

/// <summary>
/// Enregistre toutes les correspondances qui se produisent pendant une opération de recherche et de remplacement dans l'ordre dans lequel elles se produisent.
/// </summary>
private class TextReplacementRecorder : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### Voir également

* espace de noms [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../)
