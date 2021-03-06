---
title: MatchCase
second_title: Référence de l'API Aspose.Words pour .NET
description: True indique une comparaison sensible à la casse false indique une comparaison insensible à la casse.
type: docs
weight: 120
url: /fr/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse.

```csharp
public bool MatchCase { get; set; }
```

### Exemples

Montre comment activer/désactiver la sensibilité à la casse lors de l'exécution d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez le drapeau "MatchCase" sur "true" pour appliquer la sensibilité à la casse lors de la recherche des chaînes à remplacer.
// Définissez le drapeau "MatchCase" sur "false" pour ignorer la casse des caractères lors de la recherche de texte à remplacer.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../../findreplaceoptions)
* espace de noms [Aspose.Words.Replacing](../../findreplaceoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
