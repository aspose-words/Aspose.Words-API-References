---
title: DefaultFontSubstitutionRule class
linktitle: DefaultFontSubstitutionRule class
articleTitle: DefaultFontSubstitutionRule class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.DefaultFontSubstitutionRule class. Default font substitution rule"
type: docs
weight: 10
url: /tr/python-net/aspose.words.fonts/defaultfontsubstitutionrule/
---

## DefaultFontSubstitutionRule class

Default font substitution rule.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Remarks

This rule defines single default font name to be used for substitution if the original font is not available.


**Inheritance:** [DefaultFontSubstitutionRule](./) → [FontSubstitutionRule](../fontsubstitutionrule/)

### Properties

| Name | Description |
| --- | --- |
| [default_font_name](./default_font_name/) | Gets or sets the default font name. |
| [enabled](../fontsubstitutionrule/enabled/) | Specifies whether the rule is enabled or not.<br>(Inherited from [FontSubstitutionRule](../fontsubstitutionrule/)) |

### Examples

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# FontSettings içinde varsayılan ikame kuralını alın.
# Bu kural, eksik tüm yazı tiplerini "Times New Roman" ile değiştirecektir.
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual('Times New Roman', default_font_substitution_rule.default_font_name)
# Varsayılan yazı tipi ikamesini "Courier New" olarak ayarlayın.
default_font_substitution_rule.default_font_name = 'Courier New'
# Bir belge oluşturucu kullanarak, ikamenin gerçekleştiğini görmek için sahip olmadığımız bir yazı tipinde bazı metinler ekleyin,
# ve ardından sonucu bir PDF olarak oluşturun.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Missing Font'
builder.writeln('Line written in a missing font, which will be substituted with Courier New.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontSubstitutionRule.pdf')
```

### See Also

* module [aspose.words.fonts](../)
* class [FontSubstitutionRule](../fontsubstitutionrule/)

