---
title: ParagraphFormat.space_before property
linktitle: space_before property
articleTitle: space_before property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_before property. Gets or sets the amount of spacing (in points) before the paragraph."
type: docs
weight: 320
url: /python-net/aspose.words/paragraphformat/space_before/
---

## ParagraphFormat.space_before property

Gets or sets the amount of spacing (in points) before the paragraph.

Has no effect when [ParagraphFormat.space_before_auto](../space_before_auto/) is ``True``.

Valid values range from 0 to 1584 inclusive.



:raises System.ArgumentOutOfRangeException: Throws when argument was out of the range of valid values.
                                            

### Examples

Shows how to set automatic paragraph spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Apply a large amount of spacing before and after paragraphs that this builder will create.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24

# Set these flags to "True" to apply automatic spacing,
# effectively ignoring the spacing in the properties we set above.
# Leave them as "False" will apply our custom paragraph spacing.
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing

# Insert two paragraphs that will have spacing above and below them and save the document.
builder.writeln("Paragraph 1.")
builder.writeln("Paragraph 2.")

doc.save(ARTIFACTS_DIR + "ParagraphFormat.paragraph_spacing_auto.docx")
```

Shows how to apply no spacing between paragraphs with the same style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Apply a large amount of spacing before and after paragraphs that this builder will create.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24

# Set the "no_space_between_paragraphs_of_same_style" flag to "True" to apply
# no spacing between paragraphs with the same style, which will group similar paragraphs.
# Leave the "no_space_between_paragraphs_of_same_style" flag as "False"
# to evenly apply spacing to every paragraph.
builder.paragraph_format.no_space_between_paragraphs_of_same_style = no_space_between_paragraphs_of_same_style

builder.paragraph_format.style = doc.styles.get_by_name("Normal")
builder.writeln(f"Paragraph in the \"{builder.paragraph_format.style.name}\" style.")
builder.writeln(f"Paragraph in the \"{builder.paragraph_format.style.name}\" style.")
builder.writeln(f"Paragraph in the \"{builder.paragraph_format.style.name}\" style.")
builder.paragraph_format.style = doc.styles.get_by_name("Quote")
builder.writeln(f"Paragraph in the \"{builder.paragraph_format.style.name}\" style.")
builder.writeln(f"Paragraph in the \"{builder.paragraph_format.style.name}\" style.")
builder.paragraph_format.style = doc.styles.get_by_name("Normal")
builder.writeln(f"Paragraph in the \"{builder.paragraph_format.style.name}\" style.")
builder.writeln(f"Paragraph in the \"{builder.paragraph_format.style.name}\" style.")

doc.save(ARTIFACTS_DIR + "ParagraphFormat.paragraph_spacing_same_style.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

