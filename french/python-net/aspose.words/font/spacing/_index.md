---
title: Font.spacing property
linktitle: spacing property
articleTitle: spacing property
second_title: Aspose.Words for Python
description: "Font.spacing property. Returns or sets the spacing (in points) between characters ."
type: docs
weight: 390
url: /fr/python-net/aspose.words/font/spacing/
---

## Font.spacing property

Returns or sets the spacing (in points) between characters .


```python
@property
def spacing(self) -> float:
    ...

@spacing.setter
def spacing(self, value: float):
    ...

```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ajoutez une exécution de texte et augmentez la largeur des caractères à 150 %.
builder.font.scaling = 150
builder.writeln('Wide characters')
# Ajoutez une exécution de texte et ajoutez 1 pt d'espacement horizontal supplémentaire entre chaque caractère.
builder.font.spacing = 1
builder.writeln('Expanded by 1pt')
# Ajoutez une exécution de texte et rapprochez les caractères de 1 pt.
builder.font.spacing = -1
builder.writeln('Condensed by 1pt')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ScalingSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

