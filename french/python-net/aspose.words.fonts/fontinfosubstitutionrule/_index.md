---
title: FontInfoSubstitutionRule class
linktitle: FontInfoSubstitutionRule class
articleTitle: FontInfoSubstitutionRule class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontInfoSubstitutionRule class. Font info substitution rule"
type: docs
weight: 130
url: /fr/python-net/aspose.words.fonts/fontinfosubstitutionrule/
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
# Ouvrez un document qui contient du texte formaté avec une police qui n'existe dans aucune de nos sources de police.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Attribuez un rappel pour gérer les avertissements de substitution de police.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Définissez un nom de police par défaut et activez la substitution de police.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Les métriques de police originales doivent être utilisées après la substitution de police.
doc.layout_options.keep_original_font_metrics = True
# Nous recevrons un avertissement de substitution de police si nous enregistrons un document avec une police manquante.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words.fonts](../)
* class [FontSubstitutionRule](../fontsubstitutionrule/)

