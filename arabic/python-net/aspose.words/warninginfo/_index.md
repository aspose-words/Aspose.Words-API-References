---
title: WarningInfo class
linktitle: WarningInfo class
articleTitle: WarningInfo class
second_title: Aspose.Words for Python
description: "aspose.words.WarningInfo class. Contains information about a warning that Aspose.Words issued during document loading or saving"
type: docs
weight: 1450
url: /ar/python-net/aspose.words/warninginfo/
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
# افتح مستندًا يحتوي على نص منسق بخط غير موجود في أي من مصادر الخط لدينا.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# عيّن رد اتصال لمعالجة تحذيرات استبدال الخط.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# حدد اسم خط افتراضي وفعل استبدال الخط.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# يجب استخدام مقاييس الخط الأصلية بعد استبدال الخط.
doc.layout_options.keep_original_font_metrics = True
# سنتلقى تحذير استبدال الخط إذا حفظنا مستندًا بخط مفقود.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words](../)
* class [IWarningCallback](../iwarningcallback/)

