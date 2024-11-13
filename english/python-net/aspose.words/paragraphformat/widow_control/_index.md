---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# When we write the text that does not fit onto one page, one line may spill over onto the next page.
# The single line that ends up on the next page is called an "Orphan",
# and the previous line where the orphan broke off is called a "Widow".
# We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
# If we wish to preserve our document's dimensions, we can set this flag to "true"
# to push widows onto the same page as their respective orphans.
# Leave this flag as "false" will leave widow/orphan pairs in text.
# Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
# (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
builder.paragraph_format.widow_control = widow_control
# Insert text that produces an orphan and a widow.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

