---
title: is_dictionary_registered method
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise."
type: docs
weight: 30
url: /python-net/aspose.words/hyphenation/is_dictionary_registered/
---

## is_dictionary_registered(language) {#str}

Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise.



```python
def is_dictionary_registered(self, language: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str |  |

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

