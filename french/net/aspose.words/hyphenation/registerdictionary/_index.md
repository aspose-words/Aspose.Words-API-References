---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: Aspose.Words pour .NET
description: Améliorez facilement le traitement de texte grâce à la méthode Hyphenation RegisterDictionary. Chargez facilement des dictionnaires de césure spécifiques à chaque langue pour des résultats optimaux.
type: docs
weight: 40
url: /fr/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un flux. Lève une requête si le dictionnaire est illisible ou son format est invalide.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| language | String | Nom de langue, par exemple « en-US ». Consultez la documentation .NET pour « nom de culture » et la RFC 4646 pour plus de détails. |
| stream | Stream | Un flux pour le fichier dictionnaire au format OpenOffice. |

## Exemples

Montre comment ouvrir et enregistrer un dictionnaire à partir d'un fichier.

```csharp
public void RegisterDictionary()
{
    // Configurez un rappel qui suit les avertissements qui se produisent lors de l'enregistrement du dictionnaire de césure.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Enregistrez un dictionnaire de césure anglais (US) par flux.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Ouvrez un document avec des paramètres régionaux que Microsoft Word ne peut pas couper sur une machine anglaise, comme l'allemand.
    Document doc = new Document(MyDir + "German text.docx");

    // Pour couper ce document lors de l'enregistrement, nous avons besoin d'un dictionnaire de coupure pour le code de langue « de-CH ».
    // Ce rappel gérera la demande automatique de ce dictionnaire.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Lorsque nous enregistrons le document, la césure allemande prend effet.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Ce dictionnaire contient deux modèles identiques, ce qui déclenchera un avertissement.
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

* class [Hyphenation](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## RegisterDictionary(*string, string*) {#registerdictionary_1}

Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un fichier. L'erreur est générée si le dictionnaire est illisible ou son format est invalide.

Cette méthode peut également être utilisée pour enregistrer un dictionnaire nul afin d'empêcher[`Callback`](../callback/) d'être appelé à plusieurs reprises pour la même langue.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| language | String | Nom de langue, par exemple « en-US ». Consultez la documentation .NET pour « nom de culture » et la RFC 4646 pour plus de détails. |
| fileName | String | Un chemin vers le fichier dictionnaire au format Open Office. |

## Exemples

Montre comment enregistrer un dictionnaire de césure.

```csharp
// Un dictionnaire de césure contient une liste de chaînes qui définissent les règles de césure pour la langue du dictionnaire.
// Lorsqu'un document contient des lignes de texte dans lesquelles un mot pourrait être divisé et continué sur la ligne suivante,
// la césure recherchera dans la liste des chaînes du dictionnaire les sous-chaînes de ce mot.
// Si le dictionnaire contient une sous-chaîne, la césure divisera le mot sur deux lignes
// par la sous-chaîne et ajoutez un trait d'union à la première moitié.
// Enregistrez un fichier de dictionnaire du système de fichiers local dans les paramètres régionaux « de-CH ».
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Ouvrir un document contenant du texte avec une locale correspondant à celle de notre dictionnaire,
// et enregistrez-le dans un format à pages fixes. Le texte de ce document sera coupé.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Recharger le document après avoir désenregistré le dictionnaire,
// et enregistrez-le dans un autre PDF, qui n'aura pas de texte coupé.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

Montre comment ouvrir et enregistrer un dictionnaire à partir d'un fichier.

```csharp
public void RegisterDictionary()
{
    // Configurez un rappel qui suit les avertissements qui se produisent lors de l'enregistrement du dictionnaire de césure.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Enregistrez un dictionnaire de césure anglais (US) par flux.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Ouvrez un document avec des paramètres régionaux que Microsoft Word ne peut pas couper sur une machine anglaise, comme l'allemand.
    Document doc = new Document(MyDir + "German text.docx");

    // Pour couper ce document lors de l'enregistrement, nous avons besoin d'un dictionnaire de coupure pour le code de langue « de-CH ».
    // Ce rappel gérera la demande automatique de ce dictionnaire.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Lorsque nous enregistrons le document, la césure allemande prend effet.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Ce dictionnaire contient deux modèles identiques, ce qui déclenchera un avertissement.
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

* class [Hyphenation](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
