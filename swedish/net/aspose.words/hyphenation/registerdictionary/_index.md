---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: Aspose.Words för .NET
description: Förbättra textbehandlingen enkelt med Hyphenation RegisterDictionary-metoden. Ladda språkspecifika bindestrecksordböcker sömlöst för optimala resultat.
type: docs
weight: 40
url: /sv/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

Registrerar och laddar en bindestreckslexikon för det angivna språket från en dataström. Utlöser ett fel om lexikonet inte kan läsas eller har ett ogiltigt format.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| language | String | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "kulturnamn" och RFC 4646 för mer information. |
| stream | Stream | En ström för ordboksfilen i OpenOffice-format. |

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

* class [Hyphenation](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## RegisterDictionary(*string, string*) {#registerdictionary_1}

Registrerar och laddar en bindestreckslexikon för det angivna språket från en fil. Utlöser ett fel om lexikonet inte kan läsas eller har ett ogiltigt format.

Den här metoden kan också användas för att registrera Null-ordlistan för att förhindra[`Callback`](../callback/) från att anropas upprepade gånger för samma språk.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| language | String | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "kulturnamn" och RFC 4646 för mer information. |
| fileName | String | En sökväg till ordboksfilen i Open Office-format. |

## Exempel

Visar hur man registrerar en bindestreckslexikon.

```csharp
// En bindestreckslexikon innehåller en lista med strängar som definierar bindestrecksregler för ordbokens språk.
// När ett dokument innehåller textrader där ett ord kan delas upp och fortsätta på nästa rad,
// bindestreck söker igenom ordbokens lista med strängar efter det ordets delsträngar.
// Om ordboken innehåller en delsträng, så kommer bindestreck att dela ordet över två rader
// av delsträngen och lägg till ett bindestreck i den första halvan.
// Registrera en ordboksfil från det lokala filsystemet till språkinställningen "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öppna ett dokument som innehåller text med en språkinställning som matchar vår ordlista,
// och spara det i ett fast sidformat. Texten i det dokumentet kommer att vara avstreckad.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ladda om dokumentet efter att ordboken avregistrerats,
// och spara den i en annan PDF-fil, som inte kommer att ha bindestreckstext.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
