---
title: ShowInBalloons enumeration
linktitle: ShowInBalloons enumeration
articleTitle: ShowInBalloons enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.ShowInBalloons enumeration. Specifies which revisions are rendered in balloons."
type: docs
weight: 130
url: /it/python-net/aspose.words.layout/showinballoons/
---

## ShowInBalloons enumeration

Specifies which revisions are rendered in balloons.

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW_IN_ANNOTATIONS](../commentdisplaymode/#SHOW_IN_ANNOTATIONS).



### Members

| Name | Description |
| --- | --- |
| NONE | Renders insert, delete and format revisions inline. |
| FORMAT | Renders insert and delete revisions inline, format revisions in balloons. |
| FORMAT_AND_DELETE | Renders insert revisions inline, delete and format revisions in balloons. |

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

* module [aspose.words.layout](../)

