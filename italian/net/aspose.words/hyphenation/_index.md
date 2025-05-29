---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Hyphenation per una gestione efficiente della sillabazione. Migliora i tuoi documenti con precise regole di sillabazione specifiche per ogni lingua.
type: docs
weight: 3580
url: /it/net/aspose.words/hyphenation/
---
## Hyphenation class

Fornisce metodi per lavorare con i dizionari di sillabazione. Questi dizionari indicano dove le parole di una lingua specifica possono essere sillabate.

Per saperne di più, visita il[Lavorare con la sillabazione](https://docs.aspose.com/words/net/working-with-hyphenation/) articolo di documentazione.

```csharp
public static class Hyphenation
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Ottiene o imposta l'interfaccia di callback utilizzata per richiedere dizionari quando viene creato il layout di pagina del documento. Ciò consente il caricamento ritardato dei dizionari, il che può essere utile quando si elaborano documenti in più lingue. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Chiamato durante il caricamento di modelli di sillabazione, quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Restituisce`falso` se per la lingua specificata non è registrato alcun dizionario o se registrato è un dizionario Null,`VERO` altrimenti. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Registra e carica un dizionario di sillabazione per la lingua specificata da un flusso. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Registra e carica un dizionario di sillabazione per la lingua specificata da un file. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Annulla la registrazione di un dizionario di sillabazione per la lingua specificata. |

## Esempi

Mostra come aprire e registrare un dizionario da un file.

```csharp
public void RegisterDictionary()
{
    // Imposta un callback che tiene traccia degli avvisi che si verificano durante la registrazione del dizionario di sillabazione.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registra un dizionario di sillabazione inglese (USA) tramite stream.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Aprire un documento con impostazioni locali che Microsoft Word non può utilizzare per la sillabazione su un computer in lingua inglese, ad esempio in tedesco.
    Document doc = new Document(MyDir + "German text.docx");

    // Per unire con la sillabazione il documento al momento del salvataggio, abbiamo bisogno di un dizionario di sillabazione per il codice di lingua "de-CH".
    // Questa callback gestirà la richiesta automatica per quel dizionario.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Quando salviamo il documento, verrà applicata la sillabazione tedesca.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Questo dizionario contiene due modelli identici, che attiveranno un avviso.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// Associa i codici di lingua ISO ai nomi file del sistema locale per i file del dizionario di sillabazione.
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
