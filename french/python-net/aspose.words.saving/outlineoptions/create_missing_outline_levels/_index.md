---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /fr/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
---

## OutlineOptions.create_missing_outline_levels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``False``.




```python
@property
def create_missing_outline_levels(self) -> bool:
    ...

@create_missing_outline_levels.setter
def create_missing_outline_levels(self, value: bool):
    ...

```

### Examples

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
* class [OutlineOptions](../)

