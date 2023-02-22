---
title: Hyphenation.RegisterDictionary
second_title: Aspose.Words för .NET API Referens
description: Hyphenation metod. Registrerar och laddar en avstavningsordlista för det angivna språket från en ström. Kastar om ordboken inte kan läsas eller har ogiltigt format.
type: docs
weight: 40
url: /sv/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

Registrerar och laddar en avstavningsordlista för det angivna språket från en ström. Kastar om ordboken inte kan läsas eller har ogiltigt format.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| language | String | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "kulturnamn" och RFC 4646 för detaljer. |
| stream | Stream | En ström för ordboksfilen i OpenOffice-format. |

### Exempel

Visar hur man öppnar och registrerar en ordbok från en fil.

```csharp
{
    // Ställ in en återuppringning som spårar varningar som inträffar under registrering av avstavningslexikon.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrera en engelsk (amerikansk) avstavningsordbok efter ström.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Öppna ett dokument med en språkinställning som Microsoft Word inte får avstava på en engelsk maskin, till exempel tyska.
    Document doc = new Document(MyDir + "German text.docx");

    // För att avstava det dokumentet vid lagring behöver vi en avstavningsordbok för språkkoden "de-CH".
    // Denna återuppringning kommer att hantera den automatiska begäran för den ordboken.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // När vi sparar dokumentet kommer tysk avstavning att träda i kraft.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Denna ordbok innehåller två identiska mönster, som kommer att utlösa en varning.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Associerar ISO-språkkoder med lokala systemfilnamn för avstavningsordboksfiler.
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

### Se även

* class [Hyphenation](../)
* namnutrymme [Aspose.Words](../../hyphenation/)
* hopsättning [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

Registrerar och laddar en avstavningsordlista för det angivna språket från filen. Kastar om ordboken inte kan läsas eller har ogiltigt format.

Denna metod kan också användas för att registrera Null-ordbok för att förhindra[`Callback`](../callback/) från att bli anropade upprepade gånger för samma språk.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| language | String | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "kulturnamn" och RFC 4646 för detaljer. |
| fileName | String | En sökväg till ordboksfilen i Open Office-format. |

### Exempel

Visar hur man registrerar en avstavningsordbok.

```csharp
// En avstavningsordbok innehåller en lista med strängar som definierar avstavningsregler för ordbokens språk.
// När ett dokument innehåller textrader där ett ord kan delas upp och fortsätta på nästa rad,
// Avstavning kommer att titta igenom ordbokens lista med strängar för det ordets delsträngar.
// Om ordboken innehåller en delsträng, kommer avstavning att dela ordet över två rader
// av delsträngen och lägg till ett bindestreck till den första halvan.
// Registrera en ordboksfil från det lokala filsystemet till "de-CH"-lokalen.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öppna ett dokument som innehåller text med ett språk som matchar vår ordbok,
// och spara den i ett sparat format med fast sida. Texten i det dokumentet kommer att avstavas.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ladda om dokumentet efter avregistrering av ordboken,
// och spara den till en annan PDF, som inte kommer att ha avstavad text.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

Visar hur man öppnar och registrerar en ordbok från en fil.

```csharp
{
    // Ställ in en återuppringning som spårar varningar som inträffar under registrering av avstavningslexikon.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrera en engelsk (amerikansk) avstavningsordbok efter ström.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Öppna ett dokument med en språkinställning som Microsoft Word inte får avstava på en engelsk maskin, till exempel tyska.
    Document doc = new Document(MyDir + "German text.docx");

    // För att avstava det dokumentet vid lagring behöver vi en avstavningsordbok för språkkoden "de-CH".
    // Denna återuppringning kommer att hantera den automatiska begäran för den ordboken.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // När vi sparar dokumentet kommer tysk avstavning att träda i kraft.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Denna ordbok innehåller två identiska mönster, som kommer att utlösa en varning.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Associerar ISO-språkkoder med lokala systemfilnamn för avstavningsordboksfiler.
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

### Se även

* class [Hyphenation](../)
* namnutrymme [Aspose.Words](../../hyphenation/)
* hopsättning [Aspose.Words](../../../)


