---
title: RevisionTextEffect enumeration
linktitle: RevisionTextEffect enumeration
articleTitle: RevisionTextEffect enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.RevisionTextEffect enumeration. Allows to specify decoration effect for revisions of document text."
type: docs
weight: 120
url: /sv/python-net/aspose.words.layout/revisiontexteffect/
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
# Hämta RevisionOptions-objektet som styr utseendet på revisioner.
revision_options = doc.layout_options.revision_options
# Rendera insättningsrevisioner i grönt och kursivt.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Rendera raderingsrevisioner i rött och fetstil.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# Samma text kommer att visas två gånger i en förflyttningsrevision:
# en gång vid avresepunkten och en gång vid ankomstdestinationen.
# Rendera texten i den flyttade-från-revisionen gul med dubbel genomstrykning
# och dubbelt understruken blå vid den flyttade-till-revisionen.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Rendera formatrevisioner i mörkrött och fetstil.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Placera en tjock mörkblå stapel på vänster sida av sidan bredvid rader som påverkats av revisioner.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Visa revisionsmarkeringar och originaltext.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Få flytt-, raderings- och formateringsrevisioner samt kommentarer att visas i gröna ballonger
# på högra sidan av sidan.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# Dessa funktioner gäller endast för format som .pdf eller .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../)

