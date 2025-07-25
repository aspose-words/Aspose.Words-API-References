---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words for .NET
description: Discover the Hyphenation IsDictionaryRegistered method, checks if a dictionary is registered for your language, ensuring accurate hyphenation in your applications.
type: docs
weight: 30
url: /net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Returns `false` if for the specified language there is no dictionary registered or if registered is Null dictionary, `true` otherwise.

```csharp
public static bool IsDictionaryRegistered(string language)
```

## Examples

Shows how to register a hyphenation dictionary.

```csharp
// A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
// When a document contains lines of text in which a word could be split up and continued on the next line,
// hyphenation will look through the dictionary's list of strings for that word's substrings.
// If the dictionary contains a substring, then hyphenation will split the word across two lines
// by the substring and add a hyphen to the first half.
// Register a dictionary file from the local file system to the "de-CH" locale.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.That(Hyphenation.IsDictionaryRegistered("de-CH"), Is.True);

// Open a document containing text with a locale matching that of our dictionary,
// and save it to a fixed-page save format. The text in that document will be hyphenated.
Document doc = new Document(MyDir + "German text.docx");

Assert.That(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID), Is.True);

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Re-load the document after un-registering the dictionary,
// and save it to another PDF, which will not have hyphenated text.
Hyphenation.UnregisterDictionary("de-CH");

Assert.That(Hyphenation.IsDictionaryRegistered("de-CH"), Is.False);

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### See Also

* class [Hyphenation](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
