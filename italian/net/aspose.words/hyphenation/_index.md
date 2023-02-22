---
title: Class Hyphenation
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Hyphenation classe. Fornisce i metodi per lavorare con i dizionari di sillabazione. Questi dizionari prescrivono dove si possono sillabare le parole di una lingua specifica.
type: docs
weight: 2970
url: /it/net/aspose.words/hyphenation/
---
## Hyphenation class

Fornisce i metodi per lavorare con i dizionari di sillabazione. Questi dizionari prescrivono dove si possono sillabare le parole di una lingua specifica.

```csharp
public static class Hyphenation
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Ottiene o imposta l'interfaccia di callback utilizzata per richiedere i dizionari quando viene creato il layout di pagina del documento. Ciò consente il caricamento ritardato dei dizionari che può essere utile durante l'elaborazione di documenti in molte lingue. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Chiamato durante un pattern di sillabazione del caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà di formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(string) | Restituisce False se per la lingua specificata non è registrato alcun dizionario o se registrato è Dizionario Null, True in caso contrario. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(string, Stream) | Registra e carica un dizionario di sillabazione per la lingua specificata da un flusso. Genera se il dizionario non può essere letto o ha un formato non valido. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(string, string) | Registra e carica un dizionario di sillabazione per la lingua specificata da file. Genera se il dizionario non può essere letto o ha un formato non valido. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(string) | Annulla la registrazione di un dizionario di sillabazione per la lingua specificata. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


