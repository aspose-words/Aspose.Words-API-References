---
title: FindReplaceOptions.IgnoreFields
second_title: Référence de l'API Aspose.Words pour .NET
description: FindReplaceOptions propriété. Obtient ou définit une valeur booléenne indiquant soit dignorer le texte à lintérieur des champs. La valeur par défaut estFAUX .
type: docs
weight: 80
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Obtient ou définit une valeur booléenne indiquant soit d'ignorer le texte à l'intérieur des champs. La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreFields { get; set; }
```

### Remarques

Cette option affecte tout le champ (tous les nœuds entre FieldStart etFieldEnd).

Pour ignorer uniquement les codes de champ, veuillez utiliser l'option correspondante[`IgnoreFieldCodes`](../ignorefieldcodes/).

### Exemples

Montre comment ignorer le texte à l’intérieur des champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur "IgnoreFields" sur "true" pour obtenir la recherche et le remplacement
// opération pour ignorer le texte à l'intérieur des champs.
// Définissez l'indicateur "IgnoreFields" sur "false" pour obtenir la recherche et le remplacement.
// opération pour rechercher également du texte à l'intérieur des champs.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../findreplaceoptions/)
* Assemblée [Aspose.Words](../../../)


