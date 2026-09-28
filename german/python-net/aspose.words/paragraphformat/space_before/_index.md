---
title: ParagraphFormat.space_before property
linktitle: space_before property
articleTitle: space_before property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_before property. Gets or sets the amount of spacing (in points) before the paragraph."
type: docs
weight: 330
url: /de/python-net/aspose.words/paragraphformat/space_before/
---

## ParagraphFormat.space_before property

Gets or sets the amount of spacing (in points) before the paragraph.


```python
@property
def space_before(self) -> float:
    ...

@space_before.setter
def space_before(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Has no effect when [ParagraphFormat.space_before_auto](../space_before_auto/) is ``True``.

Valid values range from 0 to 1584 inclusive.




### Examples

Shows how to set automatic paragraph spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Wenden Sie einen großen Abstand vor und nach den Absätzen an, die dieser Builder erstellt.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Setzen Sie diese Flags auf "true", um automatischen Abstand anzuwenden,
# und ignorieren dabei effektiv den Abstand in den oben gesetzten Eigenschaften.
# Wenn sie auf "false" bleiben, wird unser benutzerdefinierter Absatzabstand angewendet.
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing
# Fügen Sie zwei Absätze ein, die oben und unten Abstand haben, und speichern Sie das Dokument.
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingAuto.docx')
```

Shows how to apply no spacing between paragraphs with the same style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Wenden Sie einen großen Abstand vor und nach den Absätzen an, die dieser Builder erstellt.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Setzen Sie das Flag "NoSpaceBetweenParagraphsOfSameStyle" auf "true", um anzuwenden
# keinen Abstand zwischen Absätzen mit demselben Stil, wodurch ähnliche Absätze gruppiert werden.
# Lassen Sie das Flag "NoSpaceBetweenParagraphsOfSameStyle" auf "false"
# um den Abstand gleichmäßig auf jeden Absatz anzuwenden.
builder.paragraph_format.no_space_between_paragraphs_of_same_style = no_space_between_paragraphs_of_same_style
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Quote')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingSameStyle.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

