---
title: ParagraphFormat.space_after property
linktitle: space_after property
articleTitle: space_after property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_after property. Gets or sets the amount of spacing (in points) after the paragraph."
type: docs
weight: 310
url: /es/python-net/aspose.words/paragraphformat/space_after/
---

## ParagraphFormat.space_after property

Gets or sets the amount of spacing (in points) after the paragraph.


```python
@property
def space_after(self) -> float:
    ...

@space_after.setter
def space_after(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Has no effect when [ParagraphFormat.space_after_auto](../space_after_auto/) is ``True``.

Valid values ​​range from 0 to 1584 inclusive.




### Examples

Shows how to set automatic paragraph spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Aplique una gran cantidad de espaciado antes y después de los párrafos que este generador creará.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Establezca estas banderas a "true" para aplicar espaciado automático,
# ignorando efectivamente el espaciado en las propiedades que establecimos arriba.
# Dejarlas en "false" aplicará nuestro espaciado de párrafo personalizado.
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing
# Inserte dos párrafos que tendrán espaciado arriba y abajo y guarde el documento.
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingAuto.docx')
```

Shows how to apply no spacing between paragraphs with the same style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Aplique una gran cantidad de espaciado antes y después de los párrafos que este generador creará.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Establezca la bandera "NoSpaceBetweenParagraphsOfSameStyle" a "true" para aplicar
# sin espaciado entre párrafos con el mismo estilo, lo que agrupará párrafos similares.
# Deje la bandera "NoSpaceBetweenParagraphsOfSameStyle" como "false"
# para aplicar uniformemente el espaciado a cada párrafo.
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

