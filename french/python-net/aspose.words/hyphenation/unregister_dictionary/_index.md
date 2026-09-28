---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /fr/python-net/aspose.words/hyphenation/unregister_dictionary/
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
# Un dictionnaire de césure contient une liste de chaînes qui définissent les règles de césure pour la langue du dictionnaire.
# Lorsqu'un document contient des lignes de texte dans lesquelles un mot pourrait être séparé et poursuivi sur la ligne suivante,
# la césure recherchera dans la liste de chaînes du dictionnaire les sous‑chaînes de ce mot.
# Si le dictionnaire contient une sous‑chaîne, la césure divisera le mot sur deux lignes
# à l'endroit de la sous‑chaîne et ajoutera un trait d'union à la première moitié.
# Enregistrez un fichier de dictionnaire depuis le système de fichiers local vers la locale "de-CH".
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# Ouvrez un document contenant du texte dont la locale correspond à celle de notre dictionnaire,
# et enregistrez-le dans un format d'enregistrement à page fixe. Le texte de ce document sera césuré.
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# Rechargez le document après avoir désenregistré le dictionnaire,
# et enregistrez-le dans un autre PDF, qui ne contiendra pas de texte césuré.
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

