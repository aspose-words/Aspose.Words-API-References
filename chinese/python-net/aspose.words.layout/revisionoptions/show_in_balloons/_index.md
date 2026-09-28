---
title: RevisionOptions.show_in_balloons property
linktitle: show_in_balloons property
articleTitle: show_in_balloons property
second_title: Aspose.Words for Python
description: "RevisionOptions.show_in_balloons property. Allows to specify whether the revisions are rendered in the balloons"
type: docs
weight: 180
url: /zh/python-net/aspose.words.layout/revisionoptions/show_in_balloons/
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
# 默认情况下，修订文本会使用不同的颜色，以便与其他非修订文本区分。
# 设置修订选项，在页面右侧边距的气泡中显示每个修订的更多细节。
doc.layout_options.revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT_AND_DELETE
doc.save(file_name=ARTIFACTS_DIR + 'Revision.ShowRevisionBalloons.pdf')
```

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

