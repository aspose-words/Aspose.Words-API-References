---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /es/python-net/aspose.words/hyphenation/unregister_dictionary/
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

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

