---
title: HtmlSaveOptions.document_split_heading_level property
linktitle: document_split_heading_level property
articleTitle: document_split_heading_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.document_split_heading_level property. Specifies the maximum level of headings at which to split the document"
type: docs
weight: 90
url: /es/python-net/aspose.words.saving/htmlsaveoptions/document_split_heading_level/
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
# Cada párrafo que formateamos usando un estilo "Heading" puede servir como encabezado.
# Cada encabezado también puede tener un nivel de encabezado, determinado por el número de su estilo de encabezado.
# Los encabezados a continuación son de los niveles 1-3.
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
# Cree un objeto HtmlSaveOptions y establezca el criterio de división a "HeadingParagraph".
# Estos criterios dividirán el documento en los párrafos con estilos "Heading" en varios documentos más pequeños,
# y guardarán cada documento en un archivo HTML separado en el sistema de archivos local.
# También estableceremos el nivel máximo de encabezado, lo que divide el documento a 2.
# Guardar el documento lo dividirá en los encabezados de los niveles 1 y 2, pero no en los del 3 al 9.
options = aw.saving.HtmlSaveOptions()
options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
options.document_split_heading_level = 2
# Nuestro documento tiene cuatro encabezados de los niveles 1 - 2. Uno de esos encabezados no será
# un punto de división ya que está al comienzo del documento.
# La operación de guardado dividirá nuestro documento en tres lugares, en cuatro documentos más pequeños.
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

