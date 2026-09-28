---
title: Hyphenation.register_dictionary method
linktitle: register_dictionary method
articleTitle: register_dictionary method
second_title: Aspose.Words for Python
description: "aspose.words.Hyphenation.register_dictionary method"
type: docs
weight: 40
url: /de/python-net/aspose.words/hyphenation/register_dictionary/
---

## register_dictionary(language, stream) {#str_bytesio}

Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format.


```python
def register_dictionary(self, language: str, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| stream | io.BytesIO | A stream for the dictionary file in OpenOffice format. |

## register_dictionary(language, file_name) {#str_str}

Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format.


This method can also be used to register Null dictionary to prevent[Hyphenation.callback](../callback/) from being called repeatedly for the same language.



```python
def register_dictionary(self, language: str, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| file_name | str | A path to the dictionary file in Open Office format. |

## Examples

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

## See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

