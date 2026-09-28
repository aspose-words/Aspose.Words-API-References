---
title: LayoutOptions.keep_original_font_metrics property
linktitle: keep_original_font_metrics property
articleTitle: keep_original_font_metrics property
second_title: Aspose.Words for Python
description: "LayoutOptions.keep_original_font_metrics property. Gets or sets an indication of whether the original font metrics should be used after font substitution"
type: docs
weight: 70
url: /zh/python-net/aspose.words.layout/layoutoptions/keep_original_font_metrics/
---

## LayoutOptions.keep_original_font_metrics property

Gets or sets an indication of whether the original font metrics should be used after font substitution.
Default is ``True``.



```python
@property
def keep_original_font_metrics(self) -> bool:
    ...

@keep_original_font_metrics.setter
def keep_original_font_metrics(self, value: bool):
    ...

```

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

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

