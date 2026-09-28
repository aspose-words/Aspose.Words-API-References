---
title: Paragraph.break_is_style_separator property
linktitle: break_is_style_separator property
articleTitle: break_is_style_separator property
second_title: Aspose.Words for Python
description: "Paragraph.break_is_style_separator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /fr/python-net/aspose.words/paragraph/break_is_style_separator/
---

## Paragraph.break_is_style_separator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


```python
@property
def break_is_style_separator(self) -> bool:
    ...

```

### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_table_of_contents('\\o \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Insérez un paragraphe avec un style que la TOC reconnaîtra comme une entrée.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
# Ces deux chaînes sont dans le même paragraphe et apparaîtront donc dans la même entrée de la TOC.
builder.write('Heading 1. ')
builder.write('Will appear in the TOC. ')
# Si nous insérons un séparateur de style, nous pouvons écrire plus de texte dans le même paragraphe
# et utiliser un style différent sans qu'il apparaisse dans la table des matières.
# Si nous utilisons un style de type titre après le séparateur, nous pouvons générer plusieurs entrées de la table des matières à partir d'une seule ligne de texte du document.
builder.insert_style_separator()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.QUOTE
builder.write("Won't appear in the TOC. ")
self.assertTrue(doc.first_section.body.first_paragraph.break_is_style_separator)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.BreakIsStyleSeparator.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

