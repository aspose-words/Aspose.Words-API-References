---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Textverarbeitung mühelos mit der Silbentrennungs-RegisterDictionary-Methode. Laden Sie sprachspezifische Silbentrennungswörterbücher nahtlos für optimale Ergebnisse.
type: docs
weight: 40
url: /de/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einem Stream. Wird ausgelöst, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | String | Ein Sprachname, z. B. „en-US“. Weitere Informationen zum „Kulturnamen“ finden Sie in der .NET-Dokumentation und in RFC 4646. |
| stream | Stream | Ein Stream für die Wörterbuchdatei im OpenOffice-Format. |

## Beispiele

Zeigt, wie ein Wörterbuch aus einer Datei geöffnet und registriert wird.

```csharp
public void RegisterDictionary()
{
    // Richten Sie einen Rückruf ein, der Warnungen verfolgt, die während der Registrierung des Silbentrennungswörterbuchs auftreten.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrieren Sie ein englisches (US) Silbentrennungswörterbuch per Stream.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Öffnen Sie ein Dokument mit einem Gebietsschema, das Microsoft Word auf einem englischsprachigen Computer möglicherweise nicht trennt, z. B. Deutsch.
    Document doc = new Document(MyDir + "German text.docx");

    // Um das Dokument beim Speichern mit Silbentrennung zu versehen, benötigen wir ein Silbentrennungswörterbuch für den Sprachcode „de-CH“.
    // Dieser Rückruf verarbeitet die automatische Anforderung für dieses Wörterbuch.
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
/// Verknüpft ISO-Sprachcodes mit lokalen Systemdateinamen für Silbentrennungswörterbuchdateien.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## RegisterDictionary(*string, string*) {#registerdictionary_1}

Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einer Datei. Wird ausgelöst, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat.

Diese Methode kann auch verwendet werden, um ein Null-Wörterbuch zu registrieren, um zu verhindern[`Callback`](../callback/) damit es nicht wiederholt für dieselbe Sprache aufgerufen wird.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | String | Ein Sprachname, z. B. „en-US“. Weitere Informationen zum „Kulturnamen“ finden Sie in der .NET-Dokumentation und in RFC 4646. |
| fileName | String | Ein Pfad zur Wörterbuchdatei im Open Office-Format. |

## Beispiele

Zeigt, wie ein Silbentrennungswörterbuch registriert wird.

```csharp
// Ein Silbentrennungswörterbuch enthält eine Liste von Zeichenfolgen, die Silbentrennungsregeln für die Sprache des Wörterbuchs definieren.
// Wenn ein Dokument Textzeilen enthält, in denen ein Wort aufgeteilt und in der nächsten Zeile fortgesetzt werden könnte,
// Bei der Silbentrennung wird die Zeichenfolgenliste des Wörterbuchs nach den Teilzeichenfolgen dieses Wortes durchsucht.
// Wenn das Wörterbuch eine Teilzeichenfolge enthält, wird das Wort durch die Silbentrennung auf zwei Zeilen aufgeteilt
// durch die Teilzeichenfolge und fügen Sie der ersten Hälfte einen Bindestrich hinzu.
// Registrieren Sie eine Wörterbuchdatei aus dem lokalen Dateisystem im Gebietsschema „de-CH“.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öffnen Sie ein Dokument mit Text, dessen Gebietsschema mit dem unseres Wörterbuchs übereinstimmt.
// und speichern Sie es in einem Speicherformat mit fester Seitenanzahl. Der Text in diesem Dokument wird mit Bindestrichen versehen.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Laden Sie das Dokument neu, nachdem Sie die Registrierung des Wörterbuchs aufgehoben haben.
// und speichern Sie es in einem anderen PDF, das keinen getrennten Text enthält.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

Zeigt, wie ein Wörterbuch aus einer Datei geöffnet und registriert wird.

```csharp
public void RegisterDictionary()
{
    // Richten Sie einen Rückruf ein, der Warnungen verfolgt, die während der Registrierung des Silbentrennungswörterbuchs auftreten.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrieren Sie ein englisches (US) Silbentrennungswörterbuch per Stream.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Öffnen Sie ein Dokument mit einem Gebietsschema, das Microsoft Word auf einem englischsprachigen Computer möglicherweise nicht trennt, z. B. Deutsch.
    Document doc = new Document(MyDir + "German text.docx");

    // Um das Dokument beim Speichern mit Silbentrennung zu versehen, benötigen wir ein Silbentrennungswörterbuch für den Sprachcode „de-CH“.
    // Dieser Rückruf verarbeitet die automatische Anforderung für dieses Wörterbuch.
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
/// Verknüpft ISO-Sprachcodes mit lokalen Systemdateinamen für Silbentrennungswörterbuchdateien.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
