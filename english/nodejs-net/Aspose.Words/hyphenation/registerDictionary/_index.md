---
title: Hyphenation.registerDictionary method
linktitle: registerDictionary method
articleTitle: registerDictionary method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Hyphenation.registerDictionary method"
type: docs
weight: 30
url: /nodejs-net/aspose.words/hyphenation/registerDictionary/
---

## registerDictionary(language, stream) {#string_buffer}

Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format.


```js
registerDictionary(language: string, stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | string | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| stream | Buffer | A stream for the dictionary file in OpenOffice format. |

## registerDictionary(language, fileName) {#string_string}

Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format.


This method can also be used to register Null dictionary to prevent[Hyphenation.callback](../callback/) from being called repeatedly for the same language.



```js
registerDictionary(language: string, fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | string | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| fileName | string | A path to the dictionary file in Open Office format. |

## Examples

Shows how to register a hyphenation dictionary.

```js
// A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
// When a document contains lines of text in which a word could be split up and continued on the next line,
// hyphenation will look through the dictionary's list of strings for that word's substrings.
// If the dictionary contains a substring, then hyphenation will split the word across two lines
// by the substring and add a hyphen to the first half.
// Register a dictionary file from the local file system to the "de-CH" locale.
aw.Hyphenation.registerDictionary("de-CH", base.myDir + "hyph_de_CH.dic");

expect(aw.Hyphenation.isDictionaryRegistered("de-CH")).toEqual(true);

// Open a document containing text with a locale matching that of our dictionary,
// and save it to a fixed-page save format. The text in that document will be hyphenated.
let doc = new aw.Document(base.myDir + "German text.docx");

expect(doc.firstSection.body.firstParagraph.runs.toArray().map(node => node.asRun()).All(r => r.font.localeId == new CultureInfo("de-CH").LCID)).toEqual(true);

doc.save(base.artifactsDir + "Hyphenation.Dictionary.registered.pdf");

// Re-load the document after un-registering the dictionary,
// and save it to another PDF, which will not have hyphenated text.
aw.Hyphenation.unregisterDictionary("de-CH");

expect(aw.Hyphenation.isDictionaryRegistered("de-CH")).toEqual(false);

doc = new aw.Document(base.myDir + "German text.docx");
doc.save(base.artifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

## See Also

* module [Aspose.Words](../../)
* class [Hyphenation](../)

