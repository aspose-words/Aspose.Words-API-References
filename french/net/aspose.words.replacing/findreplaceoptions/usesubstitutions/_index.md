---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words pour .NET
description: Découvrez la propriété UseSubstitutions dans FindReplaceOptions. Activez facilement les substitutions dans les modèles de remplacement pour une plus grande flexibilité d'édition de texte.
type: docs
weight: 190
url: /fr/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Obtient ou définit une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. La valeur par défaut est`FAUX` .

```csharp
public bool UseSubstitutions { get; set; }
```

## Remarques

Pour plus de détails sur les éléments de substitution, veuillez consulter : https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

## Exemples

Montre comment reconnaître et utiliser les substitutions dans les modèles de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// L'utilisation du mode hérité ne prend pas en charge de nombreuses fonctionnalités avancées, nous devons donc le définir sur « false ».
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

Montre comment remplacer le texte par des substitutions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez la propriété « UseSubstitutions » sur « true » pour obtenir
// l'opération de recherche et de remplacement pour reconnaître les éléments de substitution.
// Définissez la propriété « UseSubstitutions » sur « false » pour ignorer les éléments de substitution.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
