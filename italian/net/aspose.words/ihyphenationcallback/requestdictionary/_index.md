---
title: IHyphenationCallback.RequestDictionary
linktitle: RequestDictionary
articleTitle: RequestDictionary
second_title: Aspose.Words per .NET
description: Scopri il metodo RequestDictionary IHyphenationCallback e gestisci in modo efficiente i dizionari di sillabazione mancanti per un supporto linguistico ottimale nella tua applicazione.
type: docs
weight: 10
url: /it/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

Notifica all'applicazione che il dizionario di sillabazione per la lingua specificata non è stato trovato e potrebbe essere necessario registrarlo.

L'implementazione dovrebbe trovare un dizionario e registrarlo utilizzando[`RegisterDictionary`](../../hyphenation/registerdictionary/) metodi.

Se il dizionario non è disponibile per l'implementazione della lingua specificata, è possibile rinunciare a ulteriori chiamate per la stessa lingua utilizzando[`RegisterDictionary`](../../hyphenation/registerdictionary/) con`null` valore.

```csharp
public void RequestDictionary(string language)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| language | String | Un nome di lingua, ad esempio "en-US". Per i dettagli, vedere la documentazione .NET per il "nome della cultura" e RFC 4646. |

## Osservazioni

Le eccezioni generate da questo metodo interromperanno l'esecuzione del processo di impaginazione.

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

* interface [IHyphenationCallback](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
