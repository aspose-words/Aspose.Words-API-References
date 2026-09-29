---
title: Hyphenation.register_dictionary method
linktitle: register_dictionary method
articleTitle: register_dictionary method
second_title: Aspose.Words for Python
description: "aspose.words.Hyphenation.register_dictionary method"
type: docs
weight: 40
url: /es/python-net/aspose.words/hyphenation/register_dictionary/
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
# Un diccionario de guionado contiene una lista de cadenas que definen reglas de guionado para el idioma del diccionario.
# Cuando un documento contiene líneas de texto en las que una palabra podría dividirse y continuar en la siguiente línea,
# el guionado buscará en la lista de cadenas del diccionario los subcadenas de esa palabra.
# Si el diccionario contiene una subcadena, entonces el guionado dividirá la palabra en dos líneas
# por la subcadena y añadirá un guion a la primera mitad.
# Registre un archivo de diccionario del sistema de archivos local al locale "de-CH".
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# Abra un documento que contenga texto con un locale que coincida con el de nuestro diccionario,
# y guárdelo en un formato de guardado de página fija. El texto en ese documento tendrá guiones.
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# Recargue el documento después de desregistrar el diccionario,
# y guárdelo en otro PDF, que no tendrá texto con guiones.
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

## See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

