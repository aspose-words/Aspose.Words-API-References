---
title: Font.all_caps property
linktitle: all_caps property
articleTitle: all_caps property
second_title: Aspose.Words for Python
description: "Font.all_caps property. True if the font is formatted as all capital letters."
type: docs
weight: 10
url: /fr/python-net/aspose.words/font/all_caps/
---

## Font.all_caps property

True if the font is formatted as all capital letters.


```python
@property
def all_caps(self) -> bool:
    ...

@all_caps.setter
def all_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# Il existe deux façons de faire afficher à un run son texte en minuscules en majuscules sans modifier le contenu.
# 1 -  Réglez le drapeau AllCaps pour afficher tous les caractères en majuscules normales :
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 -  Réglez le drapeau SmallCaps pour afficher tous les caractères en petites majuscules :
# Si un caractère est en minuscule, il apparaîtra sous sa forme majuscule
# mais aura la même hauteur que la minuscule (la hauteur x de la police).
# Les caractères qui étaient en majuscules à l'origine auront le même aspect.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

