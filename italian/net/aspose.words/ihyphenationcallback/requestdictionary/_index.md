---
title: IHyphenationCallback.RequestDictionary
second_title: Aspose.Words per .NET API Reference
description: IHyphenationCallback metodo. Notifica allapplicazione che il dizionario di sillabazione per la lingua specificata non è stato trovato e potrebbe essere necessario registrarlo.
type: docs
weight: 10
url: /it/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

Notifica all'applicazione che il dizionario di sillabazione per la lingua specificata non è stato trovato e potrebbe essere necessario registrarlo.

L'implementazione dovrebbe trovare un dizionario e registrarlo utilizzando[`RegisterDictionary`](../../hyphenation/registerdictionary/) metodi.

Se il dizionario non è disponibile per l'implementazione della lingua specificata, puoi disattivare ulteriori chiamate per la stessa lingua utilizzando[`RegisterDictionary`](../../hyphenation/registerdictionary/) con`nullo` valore.

```csharp
public void RequestDictionary(string language)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| language | String | Un nome di lingua, ad esempio "en-US". Per i dettagli, vedere la documentazione .NET per il "nome della cultura" e RFC 4646. |

### Osservazioni

Le eccezioni generate da questo metodo interromperanno l'esecuzione del processo di layout della pagina.

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

* interface [IHyphenationCallback](../)
* spazio dei nomi [Aspose.Words](../../ihyphenationcallback/)
* assemblea [Aspose.Words](../../../)


