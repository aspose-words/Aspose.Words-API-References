---
title: RevisionOptions.deleted_text_effect property
linktitle: deleted_text_effect property
articleTitle: deleted_text_effect property
second_title: Aspose.Words for Python
description: "RevisionOptions.deleted_text_effect property. Allows to specify the effect to be applied to the deleted content [RevisionType.DELETION](../../../aspose.words/revisiontype/#DELETION)"
type: docs
weight: 40
url: /ru/python-net/aspose.words.layout/revisionoptions/deleted_text_effect/
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

