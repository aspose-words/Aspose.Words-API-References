---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Hyphenation-klassen för effektiv hantering av bindestreck. Förbättra dina dokument med exakta språkspecifika bindestrecksregler.
type: docs
weight: 3580
url: /sv/net/aspose.words/hyphenation/
---
## Hyphenation class

Tillhandahåller metoder för att arbeta med bindestrecksordböcker. Dessa ordböcker föreskriver var ord från ett specifikt språk kan bindas.

För att lära dig mer, besök[Arbeta med bindestreck](https://docs.aspose.com/words/net/working-with-hyphenation/) dokumentationsartikel.

```csharp
public static class Hyphenation
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Hämtar eller ställer in callback-gränssnittet som används för att begära ordböcker när dokumentets sidlayout skapas. Detta möjliggör fördröjd inläsning av ordböcker vilket kan vara användbart vid bearbetning av dokument på många språk. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Anropas under inläsning av bindestrecksmönster, när ett problem upptäcks som kan leda till förlust av formateringstillverkning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Returer`falsk` om det inte finns någon registrerad ordbok för det angivna språket, eller om det är en nullordbok registrerad,`sann` annars. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Registrerar och laddar en bindestreckslexikon för det angivna språket från en dataström. Utlöser ett fel om lexikonet inte kan läsas eller har ett ogiltigt format. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Registrerar och laddar en bindestreckslexikon för det angivna språket från en fil. Utlöser ett fel om lexikonet inte kan läsas eller har ett ogiltigt format. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Avregistrerar en bindestreckslexikon för det angivna språket. |

## Exempel

Visar hur man öppnar och registrerar en ordbok från en fil.

```csharp
public void RegisterDictionary()
{
    // Konfigurera ett återanrop som spårar varningar som uppstår under registrering av bindestreckslexikon.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrera en engelsk (amerikansk) bindestreckslexikon efter ström.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Öppna ett dokument med en språkinställning som Microsoft Word inte får använda avstavning på en engelskspråkig dator, till exempel tyska.
    Document doc = new Document(MyDir + "German text.docx");

    // För att använda bindestreck för dokumentet när det sparas behöver vi en bindestreckslexikon för språkkoden "de-CH".
    // Denna återanropning hanterar den automatiska begäran för den ordboken.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // När vi sparar dokumentet kommer tysk bindestreck att gälla.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Denna ordbok innehåller två identiska mönster, vilket kommer att utlösa en varning.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// Associerar ISO-språkkoder med lokala systemfilnamn för bindestreckslexikonfiler.
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
