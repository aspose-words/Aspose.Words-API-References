---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /sv/python-net/aspose.words/hyphenation/unregister_dictionary/
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
# En avstavningsordbok innehåller en lista med strängar som definierar avstavningsregler för ordbokens språk.
# När ett dokument innehåller textrader där ett ord kan delas upp och fortsättas på nästa rad,
# kommer avstavning att söka igenom ordbokens lista med strängar efter det ordets delsträngar.
# Om ordboken innehåller en delsträng, kommer avstavning att dela ordet över två rader
# vid delsträngen och lägga till ett bindestreck till den första halvan.
# Registrera en ordboksfil från det lokala filsystemet till "de-CH"-lokalen.
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# Öppna ett dokument som innehåller text med en locale som matchar den i vår ordbok,
# och spara det i ett fast-sidigt sparformat. Texten i det dokumentet kommer att avstavas.
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# Läs in dokumentet igen efter att ha avregistrerat ordboken,
# och spara det till en annan PDF, som inte kommer att ha avstavad text.
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

