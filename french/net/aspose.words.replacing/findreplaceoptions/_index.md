---
title: Class FindReplaceOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Replacing.FindReplaceOptions classe. Spécifie les options pour les opérations de recherche/remplacement.
type: docs
weight: 4360
url: /fr/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Spécifie les options pour les opérations de recherche/remplacement.

```csharp
public class FindReplaceOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Default_Constructor |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## Propriétés

| Nom | La description |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Formatage du texte appliqué au nouveau contenu. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Mise en forme des paragraphes appliquée au nouveau contenu. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Sélectionne la direction de remplacement. La valeur par défaut estForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True indique que l'ancienne valeur doit être un mot autonome. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Obtient ou définit une valeur booléenne indiquant soit d'ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est`faux` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Obtient ou définit une valeur booléenne indiquant soit d'ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est`faux` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Obtient ou définit une valeur booléenne indiquant soit d'ignorer le texte à l'intérieur des champs. La valeur par défaut est`faux` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Obtient ou définit une valeur booléenne indiquant soit d'ignorer les notes de bas de page. La valeur par défaut est`faux` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Obtient ou définit une valeur booléenne indiquant soit d'ignorer le texte à l'intérieur des révisions d'insertion. La valeur par défaut est`faux` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Obtient ou définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Obtient ou définit une valeur booléenne indiquant qu'il est autorisé à remplacer le paragraphe break lorsqu'il n'y a pas de paragraphe frère suivant. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. La valeur par défaut est false. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut reconnaître et utiliser des substitutions dans les modèles de remplacement. La valeur par défaut est`faux` . |

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

Montre comment basculer les opérations autonomes de recherche et de remplacement de mots uniquement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez le drapeau "FindWholeWordsOnly" sur "true" pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez le drapeau "FindWholeWordsOnly" sur "false" pour remplacer tout le texte quel que soit son environnement.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Voir également

* espace de noms [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../)


