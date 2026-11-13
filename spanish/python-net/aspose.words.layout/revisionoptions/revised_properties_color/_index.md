---
title: RevisionOptions.revised_properties_color property
linktitle: revised_properties_color property
articleTitle: revised_properties_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.revised_properties_color property. Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT_CHANGE](../../../aspose.words/revisiontype/#FORMAT_CHANGE) Default value is [RevisionColor.NO_HIGHLIGHT](../../revisioncolor/#NO_HIGHLIGHT)."
type: docs
weight: 130
url: /es/python-net/aspose.words.layout/revisionoptions/revised_properties_color/
---

## RevisionOptions.revised_properties_color property

Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT_CHANGE](../../../aspose.words/revisiontype/#FORMAT_CHANGE)
Default value is [RevisionColor.NO_HIGHLIGHT](../../revisioncolor/#NO_HIGHLIGHT).



```python
@property
def revised_properties_color(self) -> aspose.words.layout.RevisionColor:
    ...

@revised_properties_color.setter
def revised_properties_color(self, value: aspose.words.layout.RevisionColor):
    ...

```

### Examples

Shows how to modify the appearance of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Obtenga el objeto RevisionOptions que controla la apariencia de las revisiones.
revision_options = doc.layout_options.revision_options
# Renderice las revisiones de inserción en verde y cursiva.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Renderice las revisiones de eliminación en rojo y negrita.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# El mismo texto aparecerá dos veces en una revisión de movimiento:
# una vez en el punto de partida y una vez en el destino de llegada.
# Renderice el texto en la revisión movida‑desde en amarillo con una doble tachadura
# y en azul subrayado doble en la revisión movida‑hacia.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Renderice las revisiones de formato en rojo oscuro y negrita.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Coloque una barra gruesa azul oscuro en el lado izquierdo de la página junto a las líneas afectadas por las revisiones.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Muestre marcas de revisión y texto original.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Obtenga revisiones de movimiento, eliminación, formato y comentarios para que aparezcan en globos verdes
# en el lado derecho de la página.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# Estas características solo se aplican a formatos como .pdf o .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

