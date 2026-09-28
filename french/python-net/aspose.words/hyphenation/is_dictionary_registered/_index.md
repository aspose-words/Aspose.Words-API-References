---
title: Hyphenation.is_dictionary_registered method
linktitle: is_dictionary_registered method
articleTitle: is_dictionary_registered method
second_title: Aspose.Words for Python
description: "Hyphenation.is_dictionary_registered method. Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise."
type: docs
weight: 30
url: /fr/python-net/aspose.words/hyphenation/is_dictionary_registered/
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

