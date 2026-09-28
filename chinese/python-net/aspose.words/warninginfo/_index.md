---
title: WarningInfo class
linktitle: WarningInfo class
articleTitle: WarningInfo class
second_title: Aspose.Words for Python
description: "aspose.words.WarningInfo class. Contains information about a warning that Aspose.Words issued during document loading or saving"
type: docs
weight: 1450
url: /zh/python-net/aspose.words/warninginfo/
---

## WarningInfo class

Contains information about a warning that Aspose.Words issued during document loading or saving.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Remarks

You do not create instances of this class. Objects of this class are created
and passed by Aspose.Words to the [IWarningCallback.warning()](../iwarningcallback/warning/#warninginfo) method.




### Properties

| Name | Description |
| --- | --- |
| [description](./description/) | Returns the description of the warning. |
| [source](./source/) | Returns the source of the warning. |
| [warning_type](./warning_type/) | Returns the type of the warning. |

### Examples

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# 打开一个文档，其中包含使用我们任何字体源中不存在的字体格式化的文本。
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# 为处理字体替换警告分配回调函数。
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# 设置默认字体名称并启用字体替换。
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# 字体替换后应使用原始字体度量。
doc.layout_options.keep_original_font_metrics = True
# 如果我们保存的文档缺少字体，将会收到字体替换警告。
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words](../)
* class [IWarningCallback](../iwarningcallback/)

