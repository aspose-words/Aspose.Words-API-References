---
title: Hyphenation.is_dictionary_registered method
linktitle: is_dictionary_registered method
articleTitle: is_dictionary_registered method
second_title: Aspose.Words for Python
description: "Hyphenation.is_dictionary_registered method. Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise."
type: docs
weight: 30
url: /sv/python-net/aspose.words/hyphenation/is_dictionary_registered/
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

