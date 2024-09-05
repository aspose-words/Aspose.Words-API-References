---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words for .NET
description: Aspose.Words.Hyphenation class. Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated in C#.
type: docs
weight: 3430
url: /net/aspose.words/hyphenation/
---
## Hyphenation class

Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated.

To learn more, visit the [Working with Hyphenation](https://docs.aspose.com/words/net/working-with-hyphenation/) documentation article.

```csharp
public static class Hyphenation
```

## Properties

| Name | Description |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Gets or sets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Returns `false` if for the specified language there is no dictionary registered or if registered is Null dictionary, `true` otherwise. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Unregisters a hyphenation dictionary for the specified language. |

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

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
    Document doc = new Document(MyDir + "German text.docx");

    // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
    // This callback will handle the automatic request for that dictionary.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // When we save the document, German hyphenation will take effect.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // This dictionary contains two identical patterns, which will trigger a warning.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

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
