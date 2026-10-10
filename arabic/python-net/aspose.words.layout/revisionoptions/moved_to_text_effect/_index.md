---
title: RevisionOptions.moved_to_text_effect property
linktitle: moved_to_text_effect property
articleTitle: moved_to_text_effect property
second_title: Aspose.Words for Python
description: "RevisionOptions.moved_to_text_effect property. Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../../aspose.words/revisiontype/#MOVING)"
type: docs
weight: 120
url: /ar/python-net/aspose.words.layout/revisionoptions/moved_to_text_effect/
---

## RevisionOptions.moved_to_text_effect property

Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.MOVING](../../../aspose.words/revisiontype/#MOVING).
Default value is [RevisionTextEffect.DOUBLE_UNDERLINE](../../revisiontexteffect/#DOUBLE_UNDERLINE)



```python
@property
def moved_to_text_effect(self) -> aspose.words.layout.RevisionTextEffect:
    ...

@moved_to_text_effect.setter
def moved_to_text_effect(self, value: aspose.words.layout.RevisionTextEffect):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Value of [RevisionTextEffect.HIDDEN](../../revisiontexteffect/#HIDDEN) is not allowed. |

### Examples

Shows how to modify the appearance of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# احصل على كائن RevisionOptions الذي يتحكم في مظهر المراجعات.
revision_options = doc.layout_options.revision_options
# اعرض مراجعات الإدراج باللون الأخضر ومائل.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# اعرض مراجعات الحذف باللون الأحمر وعريض.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# سيظهر النص نفسه مرتين في مراجعة النقل:
# مرة عند نقطة الانطلاق ومرة عند وجهة الوصول.
# اعرض النص في مراجعة النقل من الأصلي باللون الأصفر مع خط مزدوج عبره
# وباللون الأزرق مع خط مزدوج تحته في مراجعة النقل إلى.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# اعرض مراجعات التنسيق باللون الأحمر الداكن وعريض.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# ضع شريطًا سميكًا أزرق داكن على الجانب الأيسر من الصفحة بجوار الأسطر المتأثرة بالمراجعات.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# اعرض علامات المراجعة والنص الأصلي.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# احصل على مراجعات النقل والحذف والتنسيق، والتعليقات لتظهر في بالونات خضراء
# على الجانب الأيمن من الصفحة.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# هذه الميزات تنطبق فقط على صيغ مثل .pdf أو .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

