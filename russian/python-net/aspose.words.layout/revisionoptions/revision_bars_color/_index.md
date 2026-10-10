---
title: RevisionOptions.revision_bars_color property
linktitle: revision_bars_color property
articleTitle: revision_bars_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.revision_bars_color property. Allows to specify the color to be used for side bars that identify document lines containing revised information"
type: docs
weight: 150
url: /ru/python-net/aspose.words.layout/revisionoptions/revision_bars_color/
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
# Получите объект RevisionOptions, который управляет отображением исправлений.
revision_options = doc.layout_options.revision_options
# Отображайте вставки в зеленом цвете и курсивом.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Отображайте удаления красным цветом и полужирным шрифтом.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# Тот же текст появится дважды в ревизии перемещения:
# один раз в точке отправления и один раз в точке назначения.
# Отображайте текст в ревизии перемещения‑из желтым цветом с двойным зачеркиванием
# и двойным подчеркиванием синего цвета в ревизии перемещения‑в.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Отображайте изменения формата темно‑красным цветом и полужирным шрифтом.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Разместите толстую темно‑синюю полосу слева от страницы рядом с линиями, затронутыми исправлениями.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Показывайте метки исправлений и оригинальный текст.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Получите перемещения, удаления, изменения формата и комментарии, отображаемые в зеленых облачках
# на правой стороне страницы.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# Эти функции применимы только к форматам, таким как .pdf или .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

