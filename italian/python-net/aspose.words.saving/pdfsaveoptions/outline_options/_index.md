---
title: PdfSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 260
url: /it/python-net/aspose.words.saving/pdfsaveoptions/outline_options/
---

## PdfSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [PdfSaveOptions.outline_options](./) class.




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

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci intestazioni che possano fungere da voci dell'indice (TOC) di livello 1 e 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
save_options = aw.saving.PdfSaveOptions()
# Il documento PDF di output conterrà un sommario, che è una tabella dei contenuti che elenca le intestazioni nel corpo del documento.
# Fare clic su una voce di questa struttura ci porterà alla posizione della relativa intestazione.
# Imposta la proprietà "HeadingsOutlineLevels" a "5" per includere tutte le intestazioni di livello 5 e inferiori nella struttura.
save_options.outline_options.headings_outline_levels = 5
# Questo documento contiene intestazioni di livello 1 e 5, e nessuna intestazione di livello 2, 3 e 4.
# Il documento PDF di output tratterà i livelli di struttura 2, 3 e 4 come "mancanti".
# Imposta la proprietà "CreateMissingOutlineLevels" a "true" per includere tutti i livelli mancanti nella struttura,
# lasciando voci di struttura vuote poiché non ci sono intestazioni utilizzabili.
# Imposta la proprietà "CreateMissingOutlineLevels" a "false" per ignorare i livelli di struttura mancanti,
# e trattare le intestazioni di livello 5 della struttura come di livello 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

