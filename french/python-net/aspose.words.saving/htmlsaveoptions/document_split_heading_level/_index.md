---
title: HtmlSaveOptions.document_split_heading_level property
linktitle: document_split_heading_level property
articleTitle: document_split_heading_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.document_split_heading_level property. Specifies the maximum level of headings at which to split the document"
type: docs
weight: 90
url: /fr/python-net/aspose.words.saving/htmlsaveoptions/document_split_heading_level/
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
# Chaque paragraphe que nous formatons en utilisant un style "Heading" peut servir d'en-tête.
# Chaque en-tête peut également avoir un niveau d'en-tête, déterminé par le nombre de son style d'en-tête.
# Les en-têtes ci-dessous sont de niveaux 1 à 3.
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
# Créez un objet HtmlSaveOptions et définissez le critère de division sur "HeadingParagraph".
# Ces critères diviseront le document aux paragraphes avec des styles "Heading" en plusieurs documents plus petits,
# et enregistreront chaque document dans un fichier HTML séparé dans le système de fichiers local.
# Nous définirons également le niveau d'en-tête maximal, ce qui divise le document à 2.
# L'enregistrement du document le divisera aux en-têtes de niveaux 1 et 2, mais pas aux niveaux 3 à 9.
options = aw.saving.HtmlSaveOptions()
options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
options.document_split_heading_level = 2
# Notre document possède quatre en-têtes de niveaux 1 à 2. L'un de ces en-têtes ne sera pas
# un point de division puisqu'il se trouve au début du document.
# L'opération d'enregistrement divisera notre document en trois endroits, en quatre documents plus petits.
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

