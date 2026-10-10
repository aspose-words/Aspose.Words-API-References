---
title: Hyphenation.is_dictionary_registered method
linktitle: is_dictionary_registered method
articleTitle: is_dictionary_registered method
second_title: Aspose.Words for Python
description: "Hyphenation.is_dictionary_registered method. Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise."
type: docs
weight: 30
url: /de/python-net/aspose.words/hyphenation/is_dictionary_registered/
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

