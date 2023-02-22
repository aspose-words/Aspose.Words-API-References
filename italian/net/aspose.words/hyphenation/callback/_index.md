---
title: Hyphenation.Callback
second_title: Aspose.Words per .NET API Reference
description: Hyphenation proprietà. Ottiene o imposta linterfaccia di callback utilizzata per richiedere i dizionari quando viene creato il layout di pagina del documento. Ciò consente il caricamento ritardato dei dizionari che può essere utile durante lelaborazione di documenti in molte lingue.
type: docs
weight: 10
url: /it/net/aspose.words/hyphenation/callback/
---
## Hyphenation.Callback property

Ottiene o imposta l'interfaccia di callback utilizzata per richiedere i dizionari quando viene creato il layout di pagina del documento. Ciò consente il caricamento ritardato dei dizionari che può essere utile durante l'elaborazione di documenti in molte lingue.

```csharp
public static IHyphenationCallback Callback { get; set; }
```

### Esempi

Mostra come aprire e registrare un dizionario da un file.

```csharp
{
    // Imposta una richiamata che tiene traccia degli avvisi che si verificano durante la registrazione del dizionario di sillabazione.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registra un dizionario di sillabazione inglese (Stati Uniti) tramite stream.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Apre un documento con una lingua che Microsoft Word potrebbe non sillabare su un computer inglese, come il tedesco.
    Document doc = new Document(MyDir + "German text.docx");

    // Per sillabare quel documento dopo il salvataggio, abbiamo bisogno di un dizionario di sillabazione per il codice della lingua "de-CH".
    // Questa richiamata gestirà la richiesta automatica per quel dizionario.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Quando salviamo il documento, la sillabazione tedesca avrà effetto.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Questo dizionario contiene due modelli identici, che attiveranno un avviso.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Associa i codici della lingua ISO ai nomi dei file di sistema locali per i file del dizionario di sillabazione.
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

### Guarda anche

* interface [IHyphenationCallback](../../ihyphenationcallback/)
* class [Hyphenation](../)
* spazio dei nomi [Aspose.Words](../../hyphenation/)
* assemblea [Aspose.Words](../../../)


