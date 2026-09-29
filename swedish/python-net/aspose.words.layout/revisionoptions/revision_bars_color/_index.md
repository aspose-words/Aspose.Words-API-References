---
title: RevisionOptions.revision_bars_color property
linktitle: revision_bars_color property
articleTitle: revision_bars_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.revision_bars_color property. Allows to specify the color to be used for side bars that identify document lines containing revised information"
type: docs
weight: 150
url: /sv/python-net/aspose.words.layout/revisionoptions/revision_bars_color/
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

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

