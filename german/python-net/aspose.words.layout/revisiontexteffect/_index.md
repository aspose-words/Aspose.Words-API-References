---
title: RevisionTextEffect enumeration
linktitle: RevisionTextEffect enumeration
articleTitle: RevisionTextEffect enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.RevisionTextEffect enumeration. Allows to specify decoration effect for revisions of document text."
type: docs
weight: 120
url: /de/python-net/aspose.words.layout/revisiontexteffect/
---

## RevisionTextEffect enumeration

Allows to specify decoration effect for revisions of document text.


### Members

| Name | Description |
| --- | --- |
| NONE | Revised content has no special effects applied. This corresponds to [RevisionColor.NO_HIGHLIGHT](../revisioncolor/#NO_HIGHLIGHT). |
| COLOR | Revised content is highlighted with color only. |
| BOLD | Revised content is made bold and colored. |
| ITALIC | Revised content is made italic and colored. |
| UNDERLINE | Revised content is underlined and colored. |
| DOUBLE_UNDERLINE | Revised content is double underlined and colored. |
| STRIKE_THROUGH | Revised content is stroked through and colored. |
| DOUBLE_STRIKE_THROUGH | Revised content is double stroked through and colored. |
| HIDDEN | Revised content is hidden. |

### Examples

Shows how to modify the appearance of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Rufen Sie das RevisionOptions-Objekt ab, das das Erscheinungsbild von Revisionen steuert.
revision_options = doc.layout_options.revision_options
# Stellen Sie Einfüge‑Revisionen in Grün und kursiv dar.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Stellen Sie Lösch‑Revisionen in Rot und fett dar.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# Der gleiche Text wird in einer Verschiebe‑Revision zweimal angezeigt:
# einmal am Ausgangspunkt und einmal am Zielort.
# Stellen Sie den Text bei der Verschiebung‑von‑Revision gelb mit doppeltem Durchstreichen dar
# und doppelt unterstrichen blau bei der Verschiebung‑zu‑Revision.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Stellen Sie Format‑Revisionen in dunkelrot und fett dar.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Platzieren Sie einen dicken dunkelblauen Balken auf der linken Seite der Seite neben den von Revisionen betroffenen Zeilen.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Zeigen Sie Revisionsmarken und den Originaltext an.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Lassen Sie Bewegungs‑, Lösch‑, Formatierungs‑Revisionen und Kommentare in grünen Sprechblasen erscheinen
# auf der rechten Seite der Seite.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# Diese Funktionen gelten nur für Formate wie .pdf oder .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../)

