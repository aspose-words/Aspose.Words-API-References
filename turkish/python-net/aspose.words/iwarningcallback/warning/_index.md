---
title: IWarningCallback.warning method
linktitle: warning method
articleTitle: warning method
second_title: Aspose.Words for Python
description: "IWarningCallback.warning method. Aspose.Words invokes this method when it encounters some issue during document loading  or saving that might result in loss of formatting or data fidelity."
type: docs
weight: 10
url: /tr/python-net/aspose.words/iwarningcallback/warning/
---

## warning(info) {#warninginfo}

Aspose.Words invokes this method when it encounters some issue during document loading 
or saving that might result in loss of formatting or data fidelity.


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
# Hiçbir font kaynağımızda bulunmayan bir fontla biçimlendirilmiş metin içeren bir belge açın.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Font değiştirme uyarılarını işlemek için bir geri çağırma (callback) atayın.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Varsayılan bir font adı belirleyin ve font değiştirmeyi etkinleştirin.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Font değiştirmeden sonra orijinal font ölçümleri kullanılmalıdır.
doc.layout_options.keep_original_font_metrics = True
# Eksik bir fontla belgeyi kaydedersek font değiştirme uyarısı alacağız.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words](../../)
* class [IWarningCallback](../)

