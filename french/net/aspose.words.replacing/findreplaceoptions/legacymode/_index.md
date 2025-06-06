---
title: FindReplaceOptions.LegacyMode
linktitle: LegacyMode
articleTitle: LegacyMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FindReplaceOptions LegacyMode pour basculer facilement l'algorithme classique de recherche/remplacement pour des fonctionnalités améliorées et une expérience utilisateur transparente.
type: docs
weight: 130
url: /fr/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Obtient ou définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé.

```csharp
public bool LegacyMode { get; set; }
```

## Remarques

Utilisez cet indicateur si vous avez besoin exactement du même comportement qu'avant l'introduction de la fonctionnalité avancée de recherche/remplacement. Notez que l'ancien algorithme ne prend pas en charge les fonctionnalités avancées telles que le remplacement par des sauts, l'application de la mise en forme, etc.

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

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
