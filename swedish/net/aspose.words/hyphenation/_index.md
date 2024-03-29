---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words för .NET
description: Aspose.Words.Hyphenation klass. Tillhandahåller metoder för att arbeta med avstavningsordböcker. Dessa ordböcker föreskriver var ord på ett specifikt språk kan avstavas i C#.
type: docs
weight: 3150
url: /sv/net/aspose.words/hyphenation/
---
## Hyphenation class

Tillhandahåller metoder för att arbeta med avstavningsordböcker. Dessa ordböcker föreskriver var ord på ett specifikt språk kan avstavas.

För att lära dig mer, besök[Arbeta med avstavning](https://docs.aspose.com/words/net/working-with-hyphenation/) dokumentationsartikel.

```csharp
public static class Hyphenation
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Hämtar eller ställer in återuppringningsgränssnitt som används för att begära ordlistor när sidlayout för dokumentet byggs. Detta tillåter fördröjning av laddning av ordböcker, vilket kan vara användbart vid bearbetning av dokument på många språk. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Anropas under en inläsning av avstavningsmönster, när ett problem upptäcks som kan resultera i förlust av formatering. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Returnerar`falsk` om det för det angivna språket inte finns någon ordbok registrerad eller om den är registrerad är Null-ordbok,`Sann` annars. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Registrerar och laddar en avstavningsordlista för det angivna språket från en ström. Kastar om ordboken inte kan läsas eller har ogiltigt format. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Registrerar och laddar en avstavningsordlista för det angivna språket från filen. Kastar om ordboken inte kan läsas eller har ogiltigt format. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Avregistrerar en avstavningsordlista för det angivna språket. |

## Exempel

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
