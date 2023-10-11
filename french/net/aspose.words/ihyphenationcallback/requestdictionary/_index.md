---
title: IHyphenationCallback.RequestDictionary
second_title: Référence de l'API Aspose.Words pour .NET
description: IHyphenationCallback méthode. Avertit lapplication que le dictionnaire de césure pour la langue spécifiée na pas été trouvé et quil doit peutêtre être enregistré.
type: docs
weight: 10
url: /fr/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

Avertit l'application que le dictionnaire de césure pour la langue spécifiée n'a pas été trouvé et qu'il doit peut-être être enregistré.

L'implémentation doit trouver un dictionnaire et l'enregistrer en utilisant[`RegisterDictionary`](../../hyphenation/registerdictionary/) méthodes.

Si le dictionnaire n'est pas disponible pour l'implémentation de la langue spécifiée, vous pouvez vous désinscrire des appels ultérieurs pour la même langue en utilisant[`RegisterDictionary`](../../hyphenation/registerdictionary/) avec`nul` valeur.

```csharp
public void RequestDictionary(string language)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| language | String | Un nom de langue, par exemple "en-US". Consultez la documentation .NET pour le « nom de la culture » et la RFC 4646 pour plus de détails. |

### Remarques

Les exceptions levées par cette méthode interrompront l'exécution du processus de mise en page.

### Exemples

Montre comment ouvrir et enregistrer un dictionnaire à partir d’un fichier.

```csharp
public void RegisterDictionary()
{
    // Configure un rappel qui suit les avertissements qui se produisent lors de l'enregistrement du dictionnaire de césure.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Enregistrez un dictionnaire de césure anglais (US) par flux.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Ouvrir un document avec des paramètres régionaux que Microsoft Word ne peut pas couper sur une machine anglaise, comme l'allemand.
    Document doc = new Document(MyDir + "German text.docx");

    // Pour couper ce document lors de l'enregistrement, nous avons besoin d'un dictionnaire de césure pour le code de langue "de-CH".
    // Ce rappel gérera la requête automatique pour ce dictionnaire.
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

* interface [IHyphenationCallback](../)
* espace de noms [Aspose.Words](../../ihyphenationcallback/)
* Assemblée [Aspose.Words](../../../)


