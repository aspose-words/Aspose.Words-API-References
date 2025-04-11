---
title: HtmlSaveOptions.document_split_heading_level property
linktitle: document_split_heading_level property
articleTitle: document_split_heading_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.document_split_heading_level property. Specifies the maximum level of headings at which to split the document"
type: docs
weight: 90
url: /python-net/aspose.words.saving/htmlsaveoptions/document_split_heading_level/
---

## HtmlSaveOptions.document_split_heading_level property

Specifies the maximum level of headings at which to split the document.
Default value is ``2``.



```python
@property
def document_split_heading_level(self) -> int:
    ...

@document_split_heading_level.setter
def document_split_heading_level(self, value: int):
    ...

```

### Remarks

When [HtmlSaveOptions.document_split_criteria](../document_split_criteria/) includes [DocumentSplitCriteria.HEADING_PARAGRAPH](../../documentsplitcriteria/#HEADING_PARAGRAPH)
and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using
**Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split.
Setting this property to zero will cause the document not to be split at heading paragraphs at all.




### Examples

Shows how to split an output HTML document by headings into several parts.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Every paragraph that we format using a "Heading" style can serve as a heading.
# Each heading may also have a heading level, determined by the number of its heading style.
# The headings below are of levels 1-3.
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #1')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #2')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #3')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #4')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #5')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #6')
# Create a HtmlSaveOptions object and set the split criteria to "HeadingParagraph".
# These criteria will split the document at paragraphs with "Heading" styles into several smaller documents,
# and save each document in a separate HTML file in the local file system.
# We will also set the maximum heading level, which splits the document to 2.
# Saving the document will split it at headings of levels 1 and 2, but not at 3 to 9.
options = aw.saving.HtmlSaveOptions()
options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
options.document_split_heading_level = 2
# Our document has four headings of levels 1 - 2. One of those headings will not be
# a split point since it is at the beginning of the document.
# The saving operation will split our document at three places, into four smaller documents.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels.html', save_options=options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels.html')
self.assertEqual('Heading #1', doc.get_text().strip())
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels-01.html')
self.assertEqual('Heading #2\r' + 'Heading #3', doc.get_text().strip())
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels-02.html')
self.assertEqual('Heading #4', doc.get_text().strip())
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels-03.html')
self.assertEqual('Heading #5\r' + 'Heading #6', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.document_split_criteria](../document_split_criteria/)
* property [HtmlSaveOptions.document_part_saving_callback](../document_part_saving_callback/)

