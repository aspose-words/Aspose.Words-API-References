---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MatchCase dans FindReplaceOptions, activez les comparaisons sensibles ou non à la casse pour une édition de texte précise. Optimisez votre flux de travail !
type: docs
weight: 140
url: /fr/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

Vrai indique une comparaison sensible à la casse, faux indique une comparaison insensible à la casse.

```csharp
public bool MatchCase { get; set; }
```

## Exemples

Montre comment basculer la sensibilité à la casse lors de l'exécution d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur « MatchCase » sur « true » pour appliquer la sensibilité à la casse lors de la recherche des chaînes à remplacer.
// Définissez l'indicateur « MatchCase » sur « false » pour ignorer la casse des caractères lors de la recherche du texte à remplacer.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
