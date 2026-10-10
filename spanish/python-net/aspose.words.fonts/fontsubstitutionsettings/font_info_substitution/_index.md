---
title: FontSubstitutionSettings.font_info_substitution property
linktitle: font_info_substitution property
articleTitle: font_info_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.font_info_substitution property. Settings related to font info substitution rule."
type: docs
weight: 30
url: /es/python-net/aspose.words.fonts/fontsubstitutionsettings/font_info_substitution/
---

## FontSubstitutionSettings.font_info_substitution property

Settings related to font info substitution rule.


```python
@property
def font_info_substitution(self) -> aspose.words.fonts.FontInfoSubstitutionRule:
    ...

```

### Examples

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# Abra un documento que contenga texto formateado con una fuente que no exista en ninguna de nuestras fuentes tipográficas.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Asigne una devolución de llamada para manejar advertencias de sustitución de fuentes.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Establezca un nombre de fuente predeterminado y habilite la sustitución de fuentes.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Las métricas de la fuente original deben usarse después de la sustitución de fuentes.
doc.layout_options.keep_original_font_metrics = True
# Obtendremos una advertencia de sustitución de fuentes si guardamos un documento con una fuente faltante.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSubstitutionSettings](../)

