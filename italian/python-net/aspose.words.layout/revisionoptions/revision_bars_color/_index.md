---
title: RevisionOptions.revision_bars_color property
linktitle: revision_bars_color property
articleTitle: revision_bars_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.revision_bars_color property. Allows to specify the color to be used for side bars that identify document lines containing revised information"
type: docs
weight: 150
url: /it/python-net/aspose.words.layout/revisionoptions/revision_bars_color/
---

## RevisionOptions.revision_bars_color property

Allows to specify the color to be used for side bars that identify document lines containing revised information.
Default value is [RevisionColor.RED](../../revisioncolor/#RED).



```python
@property
def revision_bars_color(self) -> aspose.words.layout.RevisionColor:
    ...

@revision_bars_color.setter
def revision_bars_color(self, value: aspose.words.layout.RevisionColor):
    ...

```

### Remarks

Setting this property  to [RevisionColor.BY_AUTHOR](../../revisioncolor/#BY_AUTHOR) or [RevisionColor.NO_HIGHLIGHT](../../revisioncolor/#NO_HIGHLIGHT) values
will result in hiding revision bars from the layout.


### Examples

Shows how to modify the appearance of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Ottieni l'oggetto RevisionOptions che controlla l'aspetto delle revisioni.
revision_options = doc.layout_options.revision_options
# Visualizza le revisioni di inserimento in verde e in corsivo.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Visualizza le revisioni di eliminazione in rosso e in grassetto.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# Lo stesso testo apparirà due volte in una revisione di spostamento:
# una volta al punto di partenza e una volta alla destinazione di arrivo.
# Visualizza il testo nella revisione spostata da in giallo con una doppia barratura
# e in blu con doppia sottolineatura nella revisione spostata a.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Visualizza le revisioni di formattazione in rosso scuro e in grassetto.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Posiziona una barra spessa di colore blu scuro sul lato sinistro della pagina accanto alle linee interessate dalle revisioni.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Mostra i segni di revisione e il testo originale.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Ottieni revisioni di spostamento, eliminazione, formattazione e commenti da mostrare in palloncini verdi
# sul lato destro della pagina.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# Queste funzionalità sono applicabili solo a formati come .pdf o .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

