---
title: FontInfoSubstitutionRule class
linktitle: FontInfoSubstitutionRule class
articleTitle: FontInfoSubstitutionRule class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontInfoSubstitutionRule class. Font info substitution rule"
type: docs
weight: 130
url: /zh/python-net/aspose.words.fonts/fontinfosubstitutionrule/
---

## FontInfoSubstitutionRule class

Font info substitution rule.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Remarks

According to this rule Aspose.Words evaluates all the related fields in [FontInfo](../fontinfo/) (Panose, Sig etc) for
the missing font and finds the closest match among the available font sources. If [FontInfo](../fontinfo/) is not
available for the missing font then nothing will be done.



**Inheritance:** [FontInfoSubstitutionRule](./) → [FontSubstitutionRule](../fontsubstitutionrule/)

### Properties

| Name | Description |
| --- | --- |
| [enabled](../fontsubstitutionrule/enabled/) | Specifies whether the rule is enabled or not.<br>(Inherited from [FontSubstitutionRule](../fontsubstitutionrule/)) |

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

* module [aspose.words.fonts](../)
* class [FontSubstitutionRule](../fontsubstitutionrule/)

