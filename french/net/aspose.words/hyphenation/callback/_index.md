---
title: Hyphenation.Callback
linktitle: Callback
articleTitle: Callback
second_title: Aspose.Words pour .NET
description: Hyphenation Callback propriété. Obtient ou définit linterface de rappel utilisée pour demander des dictionnaires lors de la création de la mise en page du document. Cela permet de retarder le chargement des dictionnaires ce qui peut être utile lors du traitement de documents dans de nombreuses langues en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/hyphenation/callback/
---
## Hyphenation.Callback property

Obtient ou définit l'interface de rappel utilisée pour demander des dictionnaires lors de la création de la mise en page du document. Cela permet de retarder le chargement des dictionnaires, ce qui peut être utile lors du traitement de documents dans de nombreuses langues.

```csharp
public static IHyphenationCallback Callback { get; set; }
```

## Exemples

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

* interface [IHyphenationCallback](../../ihyphenationcallback/)
* class [Hyphenation](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
