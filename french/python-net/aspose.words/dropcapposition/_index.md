---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /fr/python-net/aspose.words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| NONE | The paragraph does not have a drop cap. |
| NORMAL | The drop cap is positioned inside the text margin on the anchor paragraph. |
| MARGIN | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez un paragraphe avec une grande lettre avec laquelle le texte des deuxième et troisième paragraphes commence.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# Actuellement, les deuxième et troisième paragraphes apparaîtront sous le premier.
# Nous pouvons convertir le premier paragraphe en lettrine pour les autres paragraphes via son objet "ParagraphFormat".
# Définissez la propriété "DropCapPosition" sur "DropCapPosition.Margin" pour placer la lettrine
# à l'extérieur de la marge de page du côté gauche si notre texte est de gauche à droite.
# Définissez la propriété "DropCapPosition" sur "DropCapPosition.Normal" pour placer la lettrine à l'intérieur des marges de la page
# et pour envelopper le reste du texte autour de celle-ci.
# "DropCapPosition.None" est l'état par défaut pour tous les paragraphes.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

