﻿---
title: RevisionOptions.revised_properties_color property
linktitle: revised_properties_color property
articleTitle: revised_properties_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.revised_properties_color property. Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT_CHANGE](../../../aspose.words/revisiontype/#FORMAT_CHANGE) Default value is [RevisionColor.NO_HIGHLIGHT](../../revisioncolor/#NO_HIGHLIGHT)."
type: docs
weight: 130
url: /python-net/aspose.words.layout/revisionoptions/revised_properties_color/
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
# Get the RevisionOptions object that controls the appearance of revisions.
revision_options = doc.layout_options.revision_options
# Render insertion revisions in green and italic.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Render deletion revisions in red and bold.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# The same text will appear twice in a movement revision:
# once at the departure point and once at the arrival destination.
# Render the text at the moved-from revision yellow with a double strike through
# and double-underlined blue at the moved-to revision.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Render format revisions in dark red and bold.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Show revision marks and original text.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Get movement, deletion, formatting revisions, and comments to show up in green balloons
# on the right side of the page.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# These features are only applicable to formats such as .pdf or .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

