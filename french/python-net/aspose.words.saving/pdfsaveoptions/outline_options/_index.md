---
title: PdfSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 260
url: /fr/python-net/aspose.words.saving/pdfsaveoptions/outline_options/
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
# Insérez des titres pouvant servir d'entrées de TOC aux niveaux 1, 2, puis 3.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF
# Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
# Cliquer sur une entrée de ce plan nous amènera à l'emplacement de son titre respectif.
# Définissez la propriété "HeadingsOutlineLevels" sur "2" pour exclure du plan tous les titres dont le niveau est supérieur à 2.
# Les deux derniers titres que nous avons insérés ci‑dessus n'apparaîtront pas.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeadingsOutlineLevels.pdf', save_options=save_options)
```

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez des titres pouvant servir d'entrées de table des matières aux niveaux 1 et 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
save_options = aw.saving.PdfSaveOptions()
# Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
# Cliquer sur une entrée de ce plan nous amènera à l'emplacement de son titre respectif.
# Définissez la propriété "HeadingsOutlineLevels" sur "5" pour inclure tous les titres des niveaux 5 et inférieurs dans le plan.
save_options.outline_options.headings_outline_levels = 5
# Ce document contient des titres des niveaux 1 et 5, et aucun titre des niveaux 2, 3 et 4.
# Le document PDF de sortie traitera les niveaux de plan 2, 3 et 4 comme "manquants".
# Définissez la propriété "CreateMissingOutlineLevels" sur "true" pour inclure tous les niveaux manquants dans le plan,
# laissant des entrées de plan vides puisqu'il n'y a aucun titre exploitable.
# Définissez la propriété "CreateMissingOutlineLevels" sur "false" pour ignorer les niveaux de plan manquants,
# et traiter les titres du niveau de plan 5 comme niveau 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

