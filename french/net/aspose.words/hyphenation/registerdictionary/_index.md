---
title: Hyphenation.RegisterDictionary
second_title: Référence de l'API Aspose.Words pour .NET
description: Hyphenation méthode. Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir dun flux. Lance si le dictionnaire ne peut pas être lu ou a un format invalide.
type: docs
weight: 40
url: /fr/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un flux. Lance si le dictionnaire ne peut pas être lu ou a un format invalide.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| language | String | Un nom de langue, par exemple "en-US". Voir la documentation .NET pour "nom de culture" et RFC 4646 pour plus de détails. |
| stream | Stream | Un flux pour le fichier de dictionnaire au format OpenOffice. |

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

* class [Hyphenation](../)
* espace de noms [Aspose.Words](../../hyphenation/)
* Assemblée [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir du fichier. Lance si le dictionnaire ne peut pas être lu ou a un format invalide.

Cette méthode peut également être utilisée pour enregistrer un dictionnaire nul afin d'empêcher[`Callback`](../callback/) d'être appelé à plusieurs reprises pour la même langue.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| language | String | Un nom de langue, par exemple "en-US". Voir la documentation .NET pour "nom de culture" et RFC 4646 pour plus de détails. |
| fileName | String | Un chemin d'accès au fichier de dictionnaire au format Open Office. |

### Exemples

Montre comment enregistrer un dictionnaire de césure.

```csharp
// Un dictionnaire de césure contient une liste de chaînes qui définissent les règles de césure pour la langue du dictionnaire.
// Lorsqu'un document contient des lignes de texte dans lesquelles un mot peut être fractionné et continué sur la ligne suivante,
// la césure recherchera dans la liste des chaînes du dictionnaire les sous-chaînes de ce mot.
// Si le dictionnaire contient une sous-chaîne, la césure divisera le mot sur deux lignes
// par la sous-chaîne et ajouter un trait d'union à la première moitié.
// Enregistre un fichier de dictionnaire du système de fichiers local dans la locale "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Ouvre un document contenant du texte avec une locale correspondant à celle de notre dictionnaire,
// et enregistrez-le dans un format de sauvegarde à page fixe. Le texte de ce document comportera un trait d'union.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Recharge le document après désenregistrement du dictionnaire,
// et enregistrez-le dans un autre PDF, qui n'aura pas de texte avec trait d'union.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* espace de noms [Aspose.Words](../../hyphenation/)
* Assemblée [Aspose.Words](../../../)


