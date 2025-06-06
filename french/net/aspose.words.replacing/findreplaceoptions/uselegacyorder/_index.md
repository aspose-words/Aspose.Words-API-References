---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words pour .NET
description: Découvrez la propriété UseLegacyOrder dans FindReplaceOptions. Activez les recherches de texte séquentielles pour une meilleure précision. La valeur par défaut est « false ». Optimisez votre traitement de texte !
type: docs
weight: 180
url: /fr/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. La valeur par défaut est`FAUX` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Exemples

Montre comment modifier l'ordre de recherche des nœuds lors de l'exécution d'une opération de recherche et de remplacement de texte.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insérez trois exécutions que nous pouvons rechercher à l'aide d'un modèle regex.
    // Placez l'une de ces exécutions dans une zone de texte.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();

    // Attribuez un rappel personnalisé à la propriété « ReplacingCallback ».
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Si nous définissons la propriété "UseLegacyOrder" sur "true", le
    // L'opération de recherche et de remplacement parcourra toutes les exécutions en dehors d'une zone de texte
    // avant de parcourir ceux à l'intérieur d'une zone de texte.
    // Si nous définissons la propriété "UseLegacyOrder" sur "false", le
    // L'opération de recherche et de remplacement parcourra toutes les exécutions d'une plage dans l'ordre séquentiel.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Enregistre l'ordre de toutes les correspondances qui se produisent au cours d'une opération de recherche et de remplacement.
/// </summary>
private class TextReplacementTracker : IReplacingCallback
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

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
