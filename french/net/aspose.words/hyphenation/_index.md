---
title: Hyphenation
second_title: Référence de l'API Aspose.Words pour .NET
description: Fournit des méthodes pour travailler avec des dictionnaires de césure. Ces dictionnaires prescrivent où les mots dune langue spécifique peuvent être coupés.
type: docs
weight: 2970
url: /fr/net/aspose.words/hyphenation/
---
## Hyphenation class

Fournit des méthodes pour travailler avec des dictionnaires de césure. Ces dictionnaires prescrivent où les mots d'une langue spécifique peuvent être coupés.

```csharp
public static class Hyphenation
```

## Propriétés

| Nom | La description |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Obtient ou définit l'interface de rappel utilisée pour demander des dictionnaires lors de la création de la mise en page du document. Cela permet de retarder le chargement des dictionnaires, ce qui peut être utile lors du traitement de documents dans de nombreuses langues. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Appelé lors d'un chargement de modèles de césure, lorsqu'un problème susceptible d'entraîner une perte de fidélité de formatage est détecté. |

## Méthodes

| Nom | La description |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(string) | Renvoie False si pour la langue spécifiée il n'y a pas de dictionnaire enregistré ou si l'enregistrement est un dictionnaire Null, True sinon. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(string, Stream) | Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un flux. Lance si le dictionnaire ne peut pas être lu ou a un format invalide. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(string, string) | Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir du fichier. Lance si le dictionnaire ne peut pas être lu ou a un format invalide. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(string) | Annule l'enregistrement d'un dictionnaire de césure pour la langue spécifiée. |

### Exemples

Montre comment ouvrir et enregistrer un dictionnaire à partir d'un fichier.

```csharp
{
    // Configurez un rappel qui suit les avertissements qui se produisent lors de l'enregistrement du dictionnaire de césure.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Enregistre un dictionnaire de césure anglais (US) par flux.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Ouvre un document avec des paramètres régionaux que Microsoft Word ne peut pas couper sur une machine anglaise, telle que l'allemand.
    Document doc = new Document(MyDir + "German text.docx");

    // Pour couper ce document lors de l'enregistrement, nous avons besoin d'un dictionnaire de césure pour le code de langue "de-CH".
    // Ce rappel gérera la demande automatique pour ce dictionnaire.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Lorsque nous enregistrons le document, la césure allemande prendra effet.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Ce dictionnaire contient deux modèles identiques, qui déclencheront un avertissement.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Associe les codes de langue ISO aux noms de fichiers du système local pour les fichiers de dictionnaire de césure.
/// </summary>
private class CustomHyphenationDictionaryRegister : IHyphenationCallback
{
    public CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = new Dictionary<string, string>
        {
            { "en-US", MyDir + "hyph_en_US.dic" },
            { "de-CH", MyDir + "hyph_de_CH.dic" }
        };
    }

    public void RequestDictionary(string language)
    {
        Console.Write("Hyphenation dictionary requested: " + language);

        if (Hyphenation.IsDictionaryRegistered(language))
        {
            Console.WriteLine(", is already registered.");
            return;
        }

        if (mHyphenationDictionaryFiles.ContainsKey(language))
        {
            Hyphenation.RegisterDictionary(language, mHyphenationDictionaryFiles[language]);
            Console.WriteLine(", successfully registered.");
            return;
        }

        Console.WriteLine(", no respective dictionary file known by this Callback.");
    }

    private readonly Dictionary<string, string> mHyphenationDictionaryFiles;
}
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
