---
title: RevisionOptions class
linktitle: RevisionOptions class
articleTitle: RevisionOptions class
second_title: Aspose.Words for Python
description: "aspose.words.layout.RevisionOptions class. Allows to control how document revisions are handled during layout process"
type: docs
weight: 110
url: /python-net/aspose.words.layout/revisionoptions/
---

## RevisionOptions class

Allows to control how document revisions are handled during layout process.
To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/python-net/converting-to-fixed-page-format/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [comment_color](./comment_color/) | Allows to specify the color to be used for comments. Default value is [RevisionColor.RED](../revisioncolor/#RED). |
| [deleted_text_color](./deleted_text_color/) | Allows to specify the color to be used for deleted content [RevisionType.DELETION](../../aspose.words/revisiontype/#DELETION). Default value is [RevisionColor.BY_AUTHOR](../revisioncolor/#BY_AUTHOR). |
| [deleted_text_effect](./deleted_text_effect/) | Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../aspose.words/revisiontype/#DELETION). Default value is [RevisionTextEffect.STRIKE_THROUGH](../revisiontexteffect/#STRIKE_THROUGH) |
| [inserted_text_color](./inserted_text_color/) | Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../aspose.words/revisiontype/#INSERTION). Default value is [RevisionColor.BY_AUTHOR](../revisioncolor/#BY_AUTHOR). |
| [inserted_text_effect](./inserted_text_effect/) | Allows to specify the effect to be applied to the inserted content [RevisionType.INSERTION](../../aspose.words/revisiontype/#INSERTION). Default value is [RevisionTextEffect.UNDERLINE](../revisiontexteffect/#UNDERLINE). |
| [measurement_unit](./measurement_unit/) | Allows to specify the measurement units for revision comments. Default value is [MeasurementUnits.CENTIMETERS](../../aspose.words/measurementunits/#CENTIMETERS) |
| [moved_from_text_color](./moved_from_text_color/) | Allows to specify the color to be used for areas where content was moved from [RevisionType.MOVING](../../aspose.words/revisiontype/#MOVING). Default value is [RevisionColor.BY_AUTHOR](../revisioncolor/#BY_AUTHOR). |
| [moved_from_text_effect](./moved_from_text_effect/) | Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.MOVING](../../aspose.words/revisiontype/#MOVING). Default value is [RevisionTextEffect.DOUBLE_STRIKE_THROUGH](../revisiontexteffect/#DOUBLE_STRIKE_THROUGH) |
| [moved_to_text_color](./moved_to_text_color/) | Allows to specify the color to be used for areas where content was moved to [RevisionType.MOVING](../../aspose.words/revisiontype/#MOVING). Default value is [RevisionColor.BY_AUTHOR](../revisioncolor/#BY_AUTHOR). |
| [moved_to_text_effect](./moved_to_text_effect/) | Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../aspose.words/revisiontype/#MOVING). Default value is [RevisionTextEffect.DOUBLE_UNDERLINE](../revisiontexteffect/#DOUBLE_UNDERLINE) |
| [revised_properties_color](./revised_properties_color/) | Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FORMAT_CHANGE](../../aspose.words/revisiontype/#FORMAT_CHANGE) Default value is [RevisionColor.NO_HIGHLIGHT](../revisioncolor/#NO_HIGHLIGHT). |
| [revised_properties_effect](./revised_properties_effect/) | Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FORMAT_CHANGE](../../aspose.words/revisiontype/#FORMAT_CHANGE) Default value is [RevisionTextEffect.NONE](../revisiontexteffect/#NONE) |
| [revision_bars_color](./revision_bars_color/) | Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is [RevisionColor.RED](../revisioncolor/#RED). |
| [revision_bars_position](./revision_bars_position/) | Gets or sets rendering position of revision bars. Default value is [HorizontalAlignment.OUTSIDE](../../aspose.words.drawing/horizontalalignment/#OUTSIDE). |
| [revision_bars_width](./revision_bars_width/) | Gets or sets width of revision bars, points. |
| [show_in_balloons](./show_in_balloons/) | Allows to specify whether the revisions are rendered in the balloons. Default value is [ShowInBalloons.NONE](../showinballoons/#NONE). |
| [show_original_revision](./show_original_revision/) | Allows to specify whether the original text should be shown instead of revised one. Default value is ``False``. |
| [show_revision_bars](./show_revision_bars/) | Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is ``True``. |
| [show_revision_marks](./show_revision_marks/) | Allow to specify whether revision text should be marked with special formatting markup. Default value is ``True``. |

### Examples

Shows how to alter the appearance of revisions in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a revision, then change the color of all revisions to green.
builder.writeln('This is not a revision.')
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
builder.writeln('This is a revision.')
doc.stop_track_revisions()
builder.writeln('This is not a revision.')
# Remove the bar that appears to the left of every revised line.
doc.layout_options.revision_options.inserted_text_color = aw.layout.RevisionColor.BRIGHT_GREEN
doc.layout_options.revision_options.show_revision_bars = False
doc.layout_options.revision_options.revision_bars_position = aw.drawing.HorizontalAlignment.RIGHT
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsRevisions.pdf')
```

### See Also

* module [aspose.words.layout](../)

