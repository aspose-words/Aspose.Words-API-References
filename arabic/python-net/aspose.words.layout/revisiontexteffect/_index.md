---
title: RevisionTextEffect enumeration
linktitle: RevisionTextEffect enumeration
articleTitle: RevisionTextEffect enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.RevisionTextEffect enumeration. Allows to specify decoration effect for revisions of document text."
type: docs
weight: 120
url: /ar/python-net/aspose.words.layout/revisiontexteffect/
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

* module [aspose.words.layout](../)

