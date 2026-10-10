---
title: ParagraphFormat.space_after property
linktitle: space_after property
articleTitle: space_after property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_after property. Gets or sets the amount of spacing (in points) after the paragraph."
type: docs
weight: 310
url: /sv/python-net/aspose.words/paragraphformat/space_after/
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
# Applicera en stor mängd avstånd före och efter stycken som denna byggare kommer att skapa.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Sätt dessa flaggor till "true" för att tillämpa automatisk avståndsjustering,
# och effektivt ignorera avståndet i de egenskaper vi satte ovan.
# Att lämna dem som "false" kommer att tillämpa vårt anpassade styckeavstånd.
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing
# Infoga två stycken som kommer att ha avstånd ovanför och nedanför dem och spara dokumentet.
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingAuto.docx')
```

Shows how to apply no spacing between paragraphs with the same style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Applicera en stor mängd avstånd före och efter stycken som denna byggare kommer att skapa.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Ställ in flaggan "NoSpaceBetweenParagraphsOfSameStyle" till "true" för att tillämpa
# inget avstånd mellan stycken med samma stil, vilket kommer att gruppera liknande stycken.
# Lämna flaggan "NoSpaceBetweenParagraphsOfSameStyle" som "false"
# för att jämnt applicera avstånd på varje stycke.
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

