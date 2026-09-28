---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /de/python-net/aspose.words/hyphenation/unregister_dictionary/
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
# Ein Silbentrennungswörterbuch enthält eine Liste von Zeichenketten, die Silbentrennungsregeln für die Sprache des Wörterbuchs definieren.
# Wenn ein Dokument Zeilen Text enthält, in denen ein Wort getrennt und in der nächsten Zeile fortgesetzt werden könnte,
# wird die Silbentrennung die Liste der Zeichenketten des Wörterbuchs nach Teilzeichenketten dieses Wortes durchsuchen.
# Wenn das Wörterbuch eine Teilzeichenkette enthält, wird die Silbentrennung das Wort über zwei Zeilen aufteilen
# nach der Teilzeichenkette und einen Bindestrich an die erste Hälfte anhängen.
# Registrieren Sie eine Wörterbuchdatei vom lokalen Dateisystem für das Locale "de-CH".
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# Öffnen Sie ein Dokument, das Text mit einem Locale enthält, das dem unseres Wörterbuchs entspricht,
# und speichern Sie es in einem Festseiten‑Speicherformat. Der Text in diesem Dokument wird silbentrennt.
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# Laden Sie das Dokument erneut, nachdem das Wörterbuch abgemeldet wurde,
# und speichern Sie es in ein weiteres PDF, das keinen silbentrennten Text enthält.
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

