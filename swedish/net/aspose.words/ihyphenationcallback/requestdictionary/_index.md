---
title: IHyphenationCallback.RequestDictionary
second_title: Aspose.Words för .NET API Referens
description: IHyphenationCallback metod. Meddelar programmet att avstavningsordbok för det angivna språket inte hittades och kan behöva registreras.
type: docs
weight: 10
url: /sv/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

Meddelar programmet att avstavningsordbok för det angivna språket inte hittades och kan behöva registreras.

Implementation bör hitta en ordbok och registrera den med hjälp av[`RegisterDictionary`](../../hyphenation/registerdictionary/) metoder.

Om ordboken inte är tillgänglig för den angivna språkimplementeringen kan du välja bort ytterligare anrop för samma språk med[`RegisterDictionary`](../../hyphenation/registerdictionary/) med`null` värde.

```csharp
public void RequestDictionary(string language)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| language | String | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "kulturnamn" och RFC 4646 för detaljer. |

### Anmärkningar

Undantag som skapas av denna metod kommer att avbryta exekvering av sidlayoutprocessen.

### Exempel

Visar hur man öppnar och registrerar en ordbok från en fil.

```csharp
public void RegisterDictionary()
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

* interface [IHyphenationCallback](../)
* namnutrymme [Aspose.Words](../../ihyphenationcallback/)
* hopsättning [Aspose.Words](../../../)


