---
title: Hyphenation.WarningCallback
second_title: Aspose.Words för .NET API Referens
description: Hyphenation fast egendom. Anropas under en inläsning av avstavningsmönster när ett problem upptäcks som kan resultera i förlust av formatering.
type: docs
weight: 20
url: /sv/net/aspose.words/hyphenation/warningcallback/
---
## Hyphenation.WarningCallback property

Anropas under en inläsning av avstavningsmönster, när ett problem upptäcks som kan resultera i förlust av formatering.

```csharp
public static IWarningCallback WarningCallback { get; set; }
```

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

* interface [IWarningCallback](../../iwarningcallback/)
* class [Hyphenation](../)
* namnutrymme [Aspose.Words](../../hyphenation/)
* hopsättning [Aspose.Words](../../../)


