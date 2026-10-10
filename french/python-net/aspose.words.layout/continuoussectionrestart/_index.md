---
title: ContinuousSectionRestart enumeration
linktitle: ContinuousSectionRestart enumeration
articleTitle: ContinuousSectionRestart enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.ContinuousSectionRestart enumeration. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering."
type: docs
weight: 20
url: /fr/python-net/aspose.words.layout/continuoussectionrestart/
---

## ContinuousSectionRestart enumeration

Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.


### Members

| Name | Description |
| --- | --- |
| ALWAYS | Page numbering always restarts regardless of content flow. |
| FROM_NEW_PAGE_ONLY | Page numbering restarts only if there is no other content before the section on the page where the section starts. |

### Examples

Shows how to control page numbering in a continuous section.

```python
doc = aw.Document(file_name=MY_DIR + 'Continuous section page numbering.docx')
# Par défaut, le comportement d'Aspose.Words correspond à Microsoft Word 2019.
# Si vous avez besoin de l'ancien comportement d'Aspose.Words, similaire à Microsoft Word 2016, utilisez 'ContinuousSectionRestart.FromNewPageOnly'.
# La numérotation des pages redémarre uniquement s'il n'y a aucun autre contenu avant la section sur la page où la section commence,
# En raison de cela, la numérotation sera réinitialisée à 2 à partir de la deuxième page.
doc.layout_options.continuous_section_page_numbering_restart = aw.layout.ContinuousSectionRestart.FROM_NEW_PAGE_ONLY
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Layout.RestartPageNumberingInContinuousSection.pdf')
```

### See Also

* module [aspose.words.layout](../)

