---
title: UnregisterDictionary
second_title: Aspose.Words for .NET API Reference
description: Hyphenation method. Unregisters a hyphenation dictionary for the specified language in C#.
type: docs
weight: 50
url: /net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Unregisters a hyphenation dictionary for the specified language.

This is different from registering Null dictionary. Unregistering a dictionary enables callback for the specified language.

```csharp
public static void UnregisterDictionary(string language)
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | String | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |

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

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Open a document containing text with a locale matching that of our dictionary,
// and save it to a fixed-page save format. The text in that document will be hyphenated.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Re-load the document after un-registering the dictionary,
// and save it to another PDF, which will not have hyphenated text.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### See Also

* class [Hyphenation](../)
* namespace [Aspose.Words](../../hyphenation/)
* assembly [Aspose.Words](../../../)
