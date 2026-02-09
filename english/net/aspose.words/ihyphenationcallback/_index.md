---
title: IHyphenationCallback Interface
linktitle: IHyphenationCallback
articleTitle: IHyphenationCallback
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.IHyphenationCallback interface to easily implement and register hyphenation dictionaries for enhanced document formatting.
type: docs
weight: 3650
url: /net/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface

Implemented by classes which can register hyphenation dictionaries.

```csharp
public interface IHyphenationCallback
```

## Methods

| Name | Description |
| --- | --- |
| [RequestDictionary](../../aspose.words/ihyphenationcallback/requestdictionary/)(*string*) | Notifies application that hyphenation dictionary for the specified language wasn't found and may need to be registered. |

## Examples

Shows how to open and register a dictionary from a file.

```csharp
public void RegisterDictionary()
{
    // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Register an English (US) hyphenation dictionary by stream.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.That(warningInfoCollection.Count, Is.EqualTo(0));

    // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
    Document doc = new Document(MyDir + "German text.docx");

    // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
    // This callback will handle the automatic request for that dictionary.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // When we save the document, German hyphenation will take effect.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // This dictionary contains two identical patterns, which will trigger a warning.
    Assert.That(warningInfoCollection.Count, Is.EqualTo(1));
    Assert.That(warningInfoCollection[0].WarningType, Is.EqualTo(WarningType.MinorFormattingLoss));
    Assert.That(warningInfoCollection[0].Source, Is.EqualTo(WarningSource.Layout));
    Assert.That(warningInfoCollection[0].Description, Is.EqualTo("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently."));

}

/// <summary>
/// Associates ISO language codes with local system filenames for hyphenation dictionary files.
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

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
