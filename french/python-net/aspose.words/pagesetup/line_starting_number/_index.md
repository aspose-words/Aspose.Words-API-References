---
title: PageSetup.line_starting_number property
linktitle: line_starting_number property
articleTitle: line_starting_number property
second_title: Aspose.Words for Python
description: "PageSetup.line_starting_number property. Gets or sets the starting line number."
type: docs
weight: 240
url: /fr/python-net/aspose.words/pagesetup/line_starting_number/
---

## PageSetup.line_starting_number property

Gets or sets the starting line number.


```python
@property
def line_starting_number(self) -> int:
    ...

@line_starting_number.setter
def line_starting_number(self, value: int):
    ...

```

### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Nous pouvons utiliser l'objet PageSetup de la section pour afficher des numéros à gauche des lignes de texte de la section.
# Ceci est le même comportement qu'un objet List,
# mais il couvre toute la section et ne modifie pas le texte de quelque manière que ce soit.
# Notre section redémarrera la numérotation sur chaque nouvelle page à partir de 1 et affichera le numéro,
# si c'est un multiple de 3, à 50 pt à gauche de la ligne.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# Le compteur de lignes sautera tout paragraphe dont le drapeau "SuppressLineNumbers" est réglé sur "true".
# Ce paragraphe se trouve sur la 15e ligne, qui est un multiple de 3, et serait donc normalement affiché avec un numéro de ligne.
# Le compteur de lignes de la section ignorera également cette ligne, considérant la ligne suivante comme la 15e,
# et continue le comptage à partir de ce point.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

