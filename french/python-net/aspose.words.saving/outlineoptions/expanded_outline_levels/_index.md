---
title: OutlineOptions.expanded_outline_levels property
linktitle: expanded_outline_levels property
articleTitle: expanded_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.expanded_outline_levels property. Specifies how many levels in the document outline to show expanded when the file is viewed."
type: docs
weight: 60
url: /fr/python-net/aspose.words.saving/outlineoptions/expanded_outline_levels/
---

## OutlineOptions.expanded_outline_levels property

Specifies how many levels in the document outline to show expanded when the file is viewed.


```python
@property
def expanded_outline_levels(self) -> int:
    ...

@expanded_outline_levels.setter
def expanded_outline_levels(self, value: int):
    ...

```

### Remarks

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items
in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez des titres de niveaux 1 à 5.
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
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
options = aw.saving.PdfSaveOptions()
# Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
# Cliquer sur une entrée de ce plan nous amènera à l'emplacement de son titre respectif.
# Définissez la propriété "HeadingsOutlineLevels" sur "4" pour exclure du plan tous les titres dont le niveau est supérieur à 4.
options.outline_options.headings_outline_levels = 4
# Si une entrée du plan possède des entrées suivantes d'un niveau supérieur entre elle et l'entrée suivante du même niveau ou d'un niveau inférieur,
# une flèche apparaîtra à gauche de l'entrée. Cette entrée est le "owner" de plusieurs "sub-entries".
# Dans notre document, les entrées du plan du cinquième niveau de titre sont des sous‑entrées de la deuxième entrée du plan de niveau quatre,
# les entrées de niveau de titre 4 et 5 sont des sous‑entrées de la deuxième entrée de niveau 3, et ainsi de suite.
# Dans le plan, nous pouvons cliquer sur la flèche de l'entrée "owner" pour réduire/étendre toutes ses sous‑entrées.
# Définissez la propriété "ExpandedOutlineLevels" à "2" pour développer automatiquement toutes les entrées du plan de niveau de titre 2 et inférieurs.
# et réduire toutes les entrées de niveau 3 et supérieures lors de l'ouverture du document.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

