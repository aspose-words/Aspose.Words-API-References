---
title: Hyphenation.RegisterDictionary
second_title: Aspose.Words per .NET API Reference
description: Hyphenation metodo. Registra e carica un dizionario di sillabazione per la lingua specificata da un flusso. Solleva un problema se il dizionario non può essere letto o ha un formato non valido.
type: docs
weight: 40
url: /it/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

Registra e carica un dizionario di sillabazione per la lingua specificata da un flusso. Solleva un problema se il dizionario non può essere letto o ha un formato non valido.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| language | String | Un nome di lingua, ad esempio "en-US". Per i dettagli, vedere la documentazione .NET per il "nome della cultura" e RFC 4646. |
| stream | Stream | Un flusso per il file dizionario in formato OpenOffice. |

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

* class [Hyphenation](../)
* spazio dei nomi [Aspose.Words](../../hyphenation/)
* assemblea [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

Registra e carica dal file un dizionario di sillabazione per la lingua specificata. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido.

Questo metodo può essere utilizzato anche per registrare il dizionario Null per impedirlo[`Callback`](../callback/) di essere chiamato ripetutamente per la stessa lingua.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| language | String | Un nome di lingua, ad esempio "en-US". Per i dettagli, vedere la documentazione .NET per il "nome della cultura" e RFC 4646. |
| fileName | String | Un percorso al file del dizionario in formato Open Office. |

### Esempi

Mostra come registrare un dizionario di sillabazione.

```csharp
// Un dizionario di sillabazione contiene un elenco di stringhe che definiscono le regole di sillabazione per la lingua del dizionario.
// Quando un documento contiene righe di testo in cui una parola può essere divisa e continuata nella riga successiva,
// la sillabazione cercherà nell'elenco di stringhe del dizionario le sottostringhe di quella parola.
// Se il dizionario contiene una sottostringa, la sillabazione dividerà la parola su due righe
// dalla sottostringa e aggiunge un trattino alla prima metà.
// Registra un file dizionario dal file system locale alla locale "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Apre un documento contenente testo con una lingua corrispondente a quella del nostro dizionario,
// e salvarlo in un formato di salvataggio a pagina fissa. Il testo in quel documento sarà sillabato.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ricarica il documento dopo aver annullato la registrazione del dizionario,
// e salvarlo in un altro PDF, che non avrà testo sillabato.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* spazio dei nomi [Aspose.Words](../../hyphenation/)
* assemblea [Aspose.Words](../../../)


