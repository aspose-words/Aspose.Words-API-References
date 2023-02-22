---
title: Hyphenation.RegisterDictionary
second_title: Aspose.Words für .NET-API-Referenz
description: Hyphenation methode. Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einem Stream. Wird ausgelöst wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat.
type: docs
weight: 40
url: /de/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einem Stream. Wird ausgelöst, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | String | Ein Sprachname, zB "en-US". Einzelheiten finden Sie in der .NET-Dokumentation für „Kulturname“ und RFC 4646. |
| stream | Stream | Ein Stream für die Wörterbuchdatei im OpenOffice-Format. |

### Beispiele

Zeigt, wie ein Wörterbuch aus einer Datei geöffnet und registriert wird.

```csharp
{
    // Richten Sie einen Rückruf ein, der Warnungen verfolgt, die während der Registrierung des Silbentrennungswörterbuchs auftreten.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrieren Sie ein englisches (US) Silbentrennungswörterbuch nach Stream.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Öffnen Sie ein Dokument mit einem Gebietsschema, das Microsoft Word auf einem englischen Computer nicht trennen darf, z. B. Deutsch.
    Document doc = new Document(MyDir + "German text.docx");

    // Um dieses Dokument beim Speichern zu trennen, benötigen wir ein Silbentrennungswörterbuch für den Sprachcode "de-CH".
    // Dieser Rückruf behandelt die automatische Anfrage für dieses Wörterbuch.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Wenn wir das Dokument speichern, wird die deutsche Silbentrennung wirksam.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Dieses Wörterbuch enthält zwei identische Muster, die eine Warnung auslösen.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Ordnet ISO-Sprachcodes lokalen Systemdateinamen für Silbentrennungswörterbuchdateien zu.
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

### Siehe auch

* class [Hyphenation](../)
* namensraum [Aspose.Words](../../hyphenation/)
* Montage [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einer Datei. Wird ausgelöst, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat.

Diese Methode kann auch verwendet werden, um die Registrierung eines Null-Wörterbuchs zu verhindern[`Callback`](../callback/) davor, wiederholt für dieselbe Sprache angerufen zu werden.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | String | Ein Sprachname, zB "en-US". Einzelheiten finden Sie in der .NET-Dokumentation für „Kulturname“ und RFC 4646. |
| fileName | String | Ein Pfad zur Wörterbuchdatei im Open Office-Format. |

### Beispiele

Zeigt, wie ein Silbentrennungswörterbuch registriert wird.

```csharp
// Ein Silbentrennungswörterbuch enthält eine Liste von Strings, die Silbentrennungsregeln für die Sprache des Wörterbuchs definieren.
// Wenn ein Dokument Textzeilen enthält, in denen ein Wort aufgeteilt und in der nächsten Zeile fortgesetzt werden könnte,
// Die Silbentrennung durchsucht die Stringliste des Wörterbuchs nach den Teilstrings dieses Wortes.
// Wenn das Wörterbuch einen Teilstring enthält, wird das Wort durch Silbentrennung auf zwei Zeilen aufgeteilt
// durch den Teilstring und füge einen Bindestrich zur ersten Hälfte hinzu.
// Registrieren Sie eine Wörterbuchdatei aus dem lokalen Dateisystem für das Gebietsschema "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öffnen Sie ein Dokument, das Text mit einem Gebietsschema enthält, das mit unserem Wörterbuch übereinstimmt,
// und in einem Festseiten-Speicherformat speichern. Der Text in diesem Dokument wird getrennt.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Laden Sie das Dokument neu, nachdem Sie das Wörterbuch abgemeldet haben,
// und in einem anderen PDF speichern, das keinen getrennten Text enthält.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

Zeigt, wie ein Wörterbuch aus einer Datei geöffnet und registriert wird.

```csharp
{
    // Richten Sie einen Rückruf ein, der Warnungen verfolgt, die während der Registrierung des Silbentrennungswörterbuchs auftreten.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrieren Sie ein englisches (US) Silbentrennungswörterbuch nach Stream.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Öffnen Sie ein Dokument mit einem Gebietsschema, das Microsoft Word auf einem englischen Computer nicht trennen darf, z. B. Deutsch.
    Document doc = new Document(MyDir + "German text.docx");

    // Um dieses Dokument beim Speichern zu trennen, benötigen wir ein Silbentrennungswörterbuch für den Sprachcode "de-CH".
    // Dieser Rückruf behandelt die automatische Anfrage für dieses Wörterbuch.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Wenn wir das Dokument speichern, wird die deutsche Silbentrennung wirksam.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Dieses Wörterbuch enthält zwei identische Muster, die eine Warnung auslösen.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Ordnet ISO-Sprachcodes lokalen Systemdateinamen für Silbentrennungswörterbuchdateien zu.
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

### Siehe auch

* class [Hyphenation](../)
* namensraum [Aspose.Words](../../hyphenation/)
* Montage [Aspose.Words](../../../)


