---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words für .NET
description: Aspose.Words.Hyphenation klas. Stellt Methoden zum Arbeiten mit Silbentrennungswörterbüchern bereit. Diese Wörterbücher schreiben vor wo Wörter einer bestimmten Sprache getrennt werden können in C#.
type: docs
weight: 3150
url: /de/net/aspose.words/hyphenation/
---
## Hyphenation class

Stellt Methoden zum Arbeiten mit Silbentrennungswörterbüchern bereit. Diese Wörterbücher schreiben vor, wo Wörter einer bestimmten Sprache getrennt werden können.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Silbentrennung](https://docs.aspose.com/words/net/working-with-hyphenation/) Dokumentationsartikel.

```csharp
public static class Hyphenation
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Ruft die Rückrufschnittstelle ab oder legt sie fest, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. Dies ermöglicht ein verzögertes Laden von Wörterbüchern, was bei der Verarbeitung von Dokumenten in vielen Sprachen nützlich sein kann. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Wird während des Ladens von Silbentrennungsmustern aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen könnte. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Gibt zurück`FALSCH` wenn für die angegebene Sprache kein Wörterbuch registriert ist oder wenn registriert ein Null-Wörterbuch ist,`WAHR` sonst. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einem Stream. Wird ausgelöst, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus der Datei. Wird ausgelöst, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Hebt die Registrierung eines Silbentrennungswörterbuchs für die angegebene Sprache auf. |

## Beispiele

Zeigt, wie man ein Wörterbuch aus einer Datei öffnet und registriert.

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

    // Öffnen Sie ein Dokument mit einem Gebietsschema, das Microsoft Word auf einem englischen Computer, z. B. Deutsch, nicht trennen darf.
    Document doc = new Document(MyDir + "German text.docx");

    // Um dieses Dokument beim Speichern zu trennen, benötigen wir ein Silbentrennungswörterbuch für den Sprachcode „de-CH“.
    // Dieser Rückruf verarbeitet die automatische Anfrage für dieses Wörterbuch.
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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
