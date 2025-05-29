---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur FindReplaceOptions pour initialiser facilement une nouvelle instance avec les paramètres par défaut, améliorant ainsi votre fonctionnalité de recherche et de remplacement.
type: docs
weight: 10
url: /fr/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

Initialise une nouvelle instance de la classe FindReplaceOptions avec les paramètres par défaut.

```csharp
public FindReplaceOptions()
```

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

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

Initialise une nouvelle instance de la classe FindReplaceOptions avec la direction spécifiée.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| direction | FindReplaceDirection | La direction de l'opération de recherche et de remplacement. |

### Voir également

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

Initialise une nouvelle instance de la classe FindReplaceOptions avec le rappel de remplacement spécifié.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | Le rappel à utiliser pour remplacer le texte trouvé. |

## Exemples

Montre comment suivre l’ordre dans lequel une opération de remplacement de texte traverse les nœuds.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // L'utilisation d'un en-tête/pied de page différent pour la première page affectera l'ordre de recherche.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Lors d'une opération de recherche et de remplacement, enregistre le contenu de chaque nœud contenant du texte que l'opération « trouve »,
/// dans l'état dans lequel il se trouve avant que le remplacement n'ait lieu.
/// Cela affichera l'ordre dans lequel l'opération de remplacement de texte traverse les nœuds.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Voir également

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

Initialise une nouvelle instance de la classe FindReplaceOptions avec la direction spécifiée et le rappel de remplacement.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| direction | FindReplaceDirection | La direction de l'opération de recherche et de remplacement. |
| replacingCallback | IReplacingCallback | Le rappel à utiliser pour remplacer le texte trouvé. |

### Voir également

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
