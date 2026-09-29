---
title: ParagraphFormat.is_heading property
linktitle: is_heading property
articleTitle: is_heading property
second_title: Aspose.Words for Python
description: "ParagraphFormat.is_heading property. True when the paragraph style is one of the built-in Heading styles."
type: docs
weight: 140
url: /it/python-net/aspose.words/paragraphformat/is_heading/
---

## ParagraphFormat.is_heading property

True when the paragraph style is one of the built-in Heading styles.


```python
@property
def is_heading(self) -> bool:
    ...

```

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci intestazioni che possano fungere da voci di indice (TOC) di livello 1, 2 e poi 3.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF
# Il documento PDF di output conterrà un sommario, che è una tabella dei contenuti che elenca le intestazioni nel corpo del documento.
# Fare clic su una voce di questa struttura ci porterà alla posizione della relativa intestazione.
# Imposta la proprietà "HeadingsOutlineLevels" su "2" per escludere tutte le intestazioni con livello superiore a 2 dalla struttura.
# Le ultime due intestazioni inserite sopra non appariranno.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeadingsOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

