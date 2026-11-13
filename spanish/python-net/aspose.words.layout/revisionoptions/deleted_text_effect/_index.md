---
title: RevisionOptions.deleted_text_effect property
linktitle: deleted_text_effect property
articleTitle: deleted_text_effect property
second_title: Aspose.Words for Python
description: "RevisionOptions.deleted_text_effect property. Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../../aspose.words/revisiontype/#DELETION)"
type: docs
weight: 40
url: /es/python-net/aspose.words.layout/revisionoptions/deleted_text_effect/
---

## RevisionOptions.deleted_text_effect property

Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../../aspose.words/revisiontype/#DELETION).
Default value is [RevisionTextEffect.STRIKE_THROUGH](../../revisiontexteffect/#STRIKE_THROUGH)



```python
@property
def deleted_text_effect(self) -> aspose.words.layout.RevisionTextEffect:
    ...

@deleted_text_effect.setter
def deleted_text_effect(self, value: aspose.words.layout.RevisionTextEffect):
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

