---
title: RevisionOptions.show_in_balloons property
linktitle: show_in_balloons property
articleTitle: show_in_balloons property
second_title: Aspose.Words for Python
description: "RevisionOptions.show_in_balloons property. Allows to specify whether the revisions are rendered in the balloons"
type: docs
weight: 180
url: /ar/python-net/aspose.words.layout/revisionoptions/show_in_balloons/
---

## RevisionOptions.show_in_balloons property

Allows to specify whether the revisions are rendered in the balloons.
Default value is [ShowInBalloons.NONE](../../showinballoons/#NONE).



```python
@property
def show_in_balloons(self) -> aspose.words.layout.ShowInBalloons:
    ...

@show_in_balloons.setter
def show_in_balloons(self, value: aspose.words.layout.ShowInBalloons):
    ...

```

### Remarks

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW_IN_ANNOTATIONS](../../commentdisplaymode/#SHOW_IN_ANNOTATIONS).



### Examples

Shows how to display revisions in balloons.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# بشكل افتراضي، النص الذي يمثل مراجعة يكون بلون مختلف لتمييزه عن النص غير المراجَع.
# عيّن خيار المراجعة لعرض مزيد من التفاصيل حول كل مراجعة في فقاعة على الهامش الأيمن للصفحة.
doc.layout_options.revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT_AND_DELETE
doc.save(file_name=ARTIFACTS_DIR + 'Revision.ShowRevisionBalloons.pdf')
```

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

