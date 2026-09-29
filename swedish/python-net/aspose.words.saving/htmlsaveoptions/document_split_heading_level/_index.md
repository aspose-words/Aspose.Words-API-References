---
title: HtmlSaveOptions.document_split_heading_level property
linktitle: document_split_heading_level property
articleTitle: document_split_heading_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.document_split_heading_level property. Specifies the maximum level of headings at which to split the document"
type: docs
weight: 90
url: /sv/python-net/aspose.words.saving/htmlsaveoptions/document_split_heading_level/
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
# Varje stycke som vi formaterar med en "Heading"-stil kan fungera som en rubrik.
# Varje rubrik kan också ha en rubriknivå, bestämd av antalet i dess rubrikstil.
# Rubrikerna nedan är på nivåerna 1-3.
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
# Skapa ett HtmlSaveOptions-objekt och sätt delningskriteriet till "HeadingParagraph".
# Detta kriterium kommer att dela dokumentet vid stycken med "Heading"-stilar i flera mindre dokument,
# och spara varje dokument i en separat HTML-fil i det lokala filsystemet.
# Vi kommer också att sätta den maximala rubriknivån, vilket delar dokumentet till 2.
# Att spara dokumentet kommer att dela det vid rubriker på nivå 1 och 2, men inte på 3 till 9.
options = aw.saving.HtmlSaveOptions()
options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
options.document_split_heading_level = 2
# Vårt dokument har fyra rubriker på nivå 1 - 2. En av dessa rubriker kommer inte att
# vara en delningspunkt eftersom den är i början av dokumentet.
# Sparningsoperationen kommer att dela vårt dokument på tre ställen, i fyra mindre dokument.
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

