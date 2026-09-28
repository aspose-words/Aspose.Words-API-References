---
title: WarningInfoCollection.warning method
linktitle: warning method
articleTitle: warning method
second_title: Aspose.Words for Python
description: "WarningInfoCollection.warning method. Implements the [IWarningCallback](../../iwarningcallback/) interface"
type: docs
weight: 50
url: /ar/python-net/aspose.words/warninginfocollection/warning/
---

## warning(info) {#warninginfo}

Implements the [IWarningCallback](../../iwarningcallback/) interface. Adds a warning to this collection.



```python
def warning(self, info: aspose.words.WarningInfo):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| info | [WarningInfo](../../warninginfo/) |  |

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

* module [aspose.words](../../)
* class [WarningInfoCollection](../)

