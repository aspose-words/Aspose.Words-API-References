---
title: IHyphenationCallback.RequestDictionary
linktitle: RequestDictionary
articleTitle: RequestDictionary
second_title: Aspose.Words für .NET
description: IHyphenationCallback RequestDictionary methode. Benachrichtigt die Anwendung dass das Silbentrennungswörterbuch für die angegebene Sprache nicht gefunden wurde und möglicherweise registriert werden muss in C#.
type: docs
weight: 10
url: /de/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

Benachrichtigt die Anwendung, dass das Silbentrennungswörterbuch für die angegebene Sprache nicht gefunden wurde und möglicherweise registriert werden muss.

Die Implementierung sollte ein Wörterbuch finden und es mit registrieren[`RegisterDictionary`](../../hyphenation/registerdictionary/) Methoden.

Wenn das Wörterbuch für die angegebene Sprachimplementierung nicht verfügbar ist, können Sie sich von weiteren Aufrufen für dieselbe Sprache abmelden[`RegisterDictionary`](../../hyphenation/registerdictionary/) mit`Null` value.

```csharp
public void RequestDictionary(string language)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | String | Ein Sprachname, z. B. „en-US“. Weitere Informationen finden Sie in der .NET-Dokumentation für „Kulturname“ und RFC 4646. |

## Bemerkungen

Von dieser Methode ausgelöste Ausnahmen brechen die Ausführung des Seitenlayoutprozesses ab.

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

* interface [IHyphenationCallback](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
