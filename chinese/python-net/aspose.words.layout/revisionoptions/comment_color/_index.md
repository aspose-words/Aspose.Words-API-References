---
title: RevisionOptions.comment_color property
linktitle: comment_color property
articleTitle: comment_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.comment_color property. Allows to specify the color to be used for comments"
type: docs
weight: 10
url: /zh/python-net/aspose.words.layout/revisionoptions/comment_color/
---

## RevisionOptions.comment_color property

Allows to specify the color to be used for comments.
Default value is [RevisionColor.RED](../../revisioncolor/#RED).



```python
@property
def comment_color(self) -> aspose.words.layout.RevisionColor:
    ...

@comment_color.setter
def comment_color(self, value: aspose.words.layout.RevisionColor):
    ...

```

### Remarks

If set this property  to [RevisionColor.BY_AUTHOR](../../revisioncolor/#BY_AUTHOR) or [RevisionColor.NO_HIGHLIGHT](../../revisioncolor/#NO_HIGHLIGHT) values,
as the result this property will be set to default color.


### Examples

Shows how to modify the appearance of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# 获取控制修订外观的 RevisionOptions 对象。
revision_options = doc.layout_options.revision_options
# 将插入修订渲染为绿色且斜体。
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# 将删除修订渲染为红色且加粗。
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# 相同的文本将在移动修订中出现两次：
# 一次在出发点，一次在到达目的地。
# 将移动前的修订文本渲染为黄色并带双删除线
# 且在移动后的修订中渲染为蓝色双下划线。
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# 将格式修订渲染为深红色且加粗。
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# 在页面左侧靠近受修订影响的行处放置一条粗暗蓝色条。
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# 显示修订标记和原始文本。
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# 获取移动、删除、格式修订和评论，使其以绿色气泡显示
# 在页面的右侧。
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# 这些功能仅适用于 .pdf 或 .jpg 等格式。
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

