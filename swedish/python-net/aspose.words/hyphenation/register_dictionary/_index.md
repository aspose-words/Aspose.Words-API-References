---
title: Hyphenation.register_dictionary method
linktitle: register_dictionary method
articleTitle: register_dictionary method
second_title: Aspose.Words for Python
description: "aspose.words.Hyphenation.register_dictionary method"
type: docs
weight: 40
url: /sv/python-net/aspose.words/hyphenation/register_dictionary/
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

## See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

