﻿---
title: ParagraphFormat.space_after_auto property
linktitle: space_after_auto property
articleTitle: space_after_auto property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_after_auto property. True if the amount of spacing after the paragraph is set automatically."
type: docs
weight: 320
url: /python-net/aspose.words/paragraphformat/space_after_auto/
---

## ParagraphFormat.space_after_auto property

True if the amount of spacing after the paragraph is set automatically.


```python
@property
def space_after_auto(self) -> bool:
    ...

@space_after_auto.setter
def space_after_auto(self, value: bool):
    ...

```

### Remarks

When set to ``True``, overrides the effect of [ParagraphFormat.space_after](../space_after/).




When you set paragraph Space Before and Space After to Auto,
Microsoft Word adds 14 points spacing between paragraphs automatically
according to the following rules:


* Normally, spacing is added after all paragraphs.
  
* In a bulleted or numbered list, spacing is added only after the last item in the list.
  Spacing is not added between the list items.
  
* In a nested bulleted or numbered list spacing is not added.
  
* Spacing is normally added after a table.
  
* Spacing is not added after a table if it is the last block in a table cell.
  
* Spacing is not added after the last paragraph in a table cell.
  



### Examples

Shows how to set automatic paragraph spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Apply a large amount of spacing before and after paragraphs that this builder will create.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Set these flags to "true" to apply automatic spacing,
# effectively ignoring the spacing in the properties we set above.
# Leave them as "false" will apply our custom paragraph spacing.
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing
# Insert two paragraphs that will have spacing above and below them and save the document.
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingAuto.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

