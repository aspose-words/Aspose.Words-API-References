---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.FindReplaceOptions pour des fonctionnalités avancées de recherche et de remplacement, améliorant l'édition de documents avec précision et flexibilité.
type: docs
weight: 5350
url: /fr/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Spécifie les options pour les opérations de recherche/remplacement.

Pour en savoir plus, visitez le[Rechercher et remplacer](https://docs.aspose.com/words/net/find-and-replace/) article de documentation.

```csharp
public class FindReplaceOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Initialise une nouvelle instance de la classe FindReplaceOptions avec les paramètres par défaut. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | Initialise une nouvelle instance de la classe FindReplaceOptions avec la direction spécifiée. |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | Initialise une nouvelle instance de la classe FindReplaceOptions avec le rappel de remplacement spécifié. |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | Initialise une nouvelle instance de la classe FindReplaceOptions avec la direction spécifiée et le rappel de remplacement. |

## Propriétés

| Nom | La description |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Mise en forme du texte appliquée au nouveau contenu. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Mise en forme de paragraphe appliquée au nouveau contenu. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Sélectionne la direction du remplacement. La valeur par défaut estForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True indique que l'ancienne valeur doit être un mot autonome. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est`FAUX` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est`FAUX` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'ignorer le texte à l'intérieur des champs. La valeur par défaut est`FAUX` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'ignorer les notes de bas de page. La valeur par défaut est`FAUX` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'ignorer le texte à l'intérieur des révisions d'insertion. La valeur par défaut est`FAUX` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'ignorer les formes dans un texte. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'ignorer le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . La valeur par défaut est`FAUX` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Obtient ou définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | Vrai indique une comparaison sensible à la casse, faux indique une comparaison insensible à la casse. |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | Spécifie le format du remplacement. La valeur par défaut estText . |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Obtient ou définit une valeur booléenne indiquant qu'il est autorisé de remplacer le paragraphe break lorsqu'il n'y a pas de paragraphe frère suivant. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. La valeur par défaut est`FAUX` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. La valeur par défaut est`FAUX` . |

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

Montre comment basculer entre les opérations de recherche et de remplacement de mots autonomes uniquement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur « FindWholeWordsOnly » sur « true » pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez l'indicateur « FindWholeWordsOnly » sur « false » pour remplacer tout le texte quel que soit son environnement.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Voir également

* espace de noms [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../)
