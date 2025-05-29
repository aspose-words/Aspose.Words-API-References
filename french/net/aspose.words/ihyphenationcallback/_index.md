---
title: IHyphenationCallback Interface
linktitle: IHyphenationCallback
articleTitle: IHyphenationCallback
second_title: Aspose.Words pour .NET
description: Explorez l'interface Aspose.Words.IHyphenationCallback pour implémenter et enregistrer facilement des dictionnaires de césure pour une mise en forme améliorée des documents.
type: docs
weight: 3630
url: /fr/net/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface

Implémenté par des classes qui peuvent enregistrer des dictionnaires de césure.

```csharp
public interface IHyphenationCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [RequestDictionary](../../aspose.words/ihyphenationcallback/requestdictionary/)(*string*) | Avertit l'application que le dictionnaire de césure pour la langue spécifiée n'a pas été trouvé et qu'il peut être nécessaire de l'enregistrer. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
