---
title: Class Hyphenation
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Hyphenation classe. Fornisce metodi per lavorare con i dizionari di sillabazione. Questi dizionari prescrivono dove le parole di una lingua specifica possono essere sillabate.
type: docs
weight: 3150
url: /it/net/aspose.words/hyphenation/
---
## Hyphenation class

Fornisce metodi per lavorare con i dizionari di sillabazione. Questi dizionari prescrivono dove le parole di una lingua specifica possono essere sillabate.

Per saperne di più, visita il[Lavorare con la sillabazione](https://docs.aspose.com/words/net/working-with-hyphenation/) articolo di documentazione.

```csharp
public static class Hyphenation
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Ottiene o imposta l'interfaccia di callback utilizzata per richiedere i dizionari quando viene creato il layout di pagina del documento. Ciò consente il caricamento ritardato dei dizionari che può essere utile durante l'elaborazione di documenti in molte lingue. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Chiamato durante il caricamento di modelli di sillabazione, quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(string) | Restituisce`falso` se per la lingua specificata non è registrato alcun dizionario o se è registrato un dizionario nullo,`VERO` altrimenti. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(string, Stream) | Registra e carica un dizionario di sillabazione per la lingua specificata da un flusso. Solleva un problema se il dizionario non può essere letto o ha un formato non valido. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(string, string) | Registra e carica dal file un dizionario di sillabazione per la lingua specificata. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(string) | Annulla la registrazione di un dizionario di sillabazione per la lingua specificata. |

### Esempi

Mostra come aprire e registrare un dizionario da un file.

```csharp
public void RegisterDictionary()
{
    // Imposta una richiamata che tiene traccia degli avvisi che si verificano durante la registrazione del dizionario di sillabazione.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registra un dizionario di sillabazione inglese (USA) per flusso.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Apre un documento con una lingua che Microsoft Word non può sillabare su un computer inglese, come il tedesco.
    Document doc = new Document(MyDir + "German text.docx");

    // Per sillabare quel documento al momento del salvataggio, abbiamo bisogno di un dizionario di sillabazione per il codice della lingua "de-CH".
    // Questa richiamata gestirà la richiesta automatica per quel dizionario.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Quando salviamo il documento, avrà effetto la sillabazione tedesca.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Questo dizionario contiene due modelli identici, che attiveranno un avviso.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Associa i codici lingua ISO ai nomi file del sistema locale per i file del dizionario di sillabazione.
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


