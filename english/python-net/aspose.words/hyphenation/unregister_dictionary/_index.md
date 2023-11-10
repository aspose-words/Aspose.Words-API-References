---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /python-net/aspose.words/hyphenation/unregister_dictionary/
---

## unregister_dictionary(language) {#str}

Unregisters a hyphenation dictionary for the specified language.


This is different from registering Null dictionary. Unregistering a dictionary enables callback for the specified language.


```python
def unregister_dictionary(self, language: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |

### Examples

Shows how to register a hyphenation dictionary.

```python
# A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
# When a document contains lines of text in which a word could be split up and continued on the next line,
# hyphenation will look through the dictionary's list of strings for that word's substrings.
# If the dictionary contains a substring, then hyphenation will split the word across two lines
# by the substring and add a hyphen to the first half.
# Register a dictionary file from the local file system to the "de-CH" locale.
aw.Hyphenation.register_dictionary("de-CH", MY_DIR + "hyph_de_CH.dic")

self.assertTrue(aw.Hyphenation.is_dictionary_registered("de-CH"))

# Open a document containing text with a locale matching that of our dictionary,
# and save it to a fixed-page save format. The text in that document will be hyphenated.
doc = aw.Document(MY_DIR + "German text.docx")

self.assertTrue(all(node for node in doc.first_section.body.first_paragraph.runs
                    if node.as_run().font.locale_id == 2055))

doc.save(ARTIFACTS_DIR + "Hyphenation.dictionary.registered.pdf")

# Re-load the document after un-registering the dictionary,
# and save it to another PDF, which will not have hyphenated text.
aw.Hyphenation.unregister_dictionary("de-CH")

self.assertFalse(aw.Hyphenation.is_dictionary_registered("de-CH"))

doc = aw.Document(MY_DIR + "German text.docx")
doc.save(ARTIFACTS_DIR + "Hyphenation.dictionary.unregistered.pdf")
```

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

