---
title: OutlineOptions.headings_outline_levels property
linktitle: headings_outline_levels property
articleTitle: headings_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.headings_outline_levels property. Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline."
type: docs
weight: 70
url: /it/python-net/aspose.words.saving/outlineoptions/headings_outline_levels/
---

## OutlineOptions.headings_outline_levels property

Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the 
document outline.


```python
@property
def headings_outline_levels(self) -> int:
    ...

@headings_outline_levels.setter
def headings_outline_levels(self, value: int):
    ...

```

### Remarks

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci intestazioni di livello da 1 a 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Il documento PDF di output conterrà un sommario, che è una tabella dei contenuti che elenca le intestazioni nel corpo del documento.
# Fare clic su una voce di questa struttura ci porterà alla posizione della relativa intestazione.
# Imposta la proprietà "HeadingsOutlineLevels" su "4" per escludere tutte le intestazioni i cui livelli sono superiori a 4 dal sommario.
options.outline_options.headings_outline_levels = 4
# Se una voce del sommario ha voci successive di livello superiore tra sé e la voce successiva dello stesso livello o inferiore,
# apparirà una freccia a sinistra della voce. Questa voce è il "owner" di diverse "sub-entries".
# Nel nostro documento, le voci del sommario dal livello di intestazione 5 sono sub-entries della seconda voce del sommario di livello 4
# le voci di livello 4 e 5 sono sotto‑voci della seconda voce di livello 3, e così via.
# Nell'indice, possiamo fare clic sulla freccia della voce "owner" per comprimere/espandere tutte le sue sotto‑voci.
# Imposta la proprietà "ExpandedOutlineLevels" a "2" per espandere automaticamente tutte le voci di indice di livello 2 e inferiori
# e comprimi tutte le voci di livello 3 e superiori quando apriamo il documento.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

