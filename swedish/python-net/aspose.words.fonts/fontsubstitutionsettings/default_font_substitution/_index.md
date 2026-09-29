---
title: FontSubstitutionSettings.default_font_substitution property
linktitle: default_font_substitution property
articleTitle: default_font_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.default_font_substitution property. Settings related to default font substitution rule."
type: docs
weight: 10
url: /sv/python-net/aspose.words.fonts/fontsubstitutionsettings/default_font_substitution/
---

## FontSubstitutionSettings.default_font_substitution property

Settings related to default font substitution rule.


```python
@property
def default_font_substitution(self) -> aspose.words.fonts.DefaultFontSubstitutionRule:
    ...

```

### Examples

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# Hämta standardsubstitutionsregeln i FontSettings.
# Denna regel kommer att ersätta alla saknade teckensnitt med "Times New Roman".
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual('Times New Roman', default_font_substitution_rule.default_font_name)
# Ställ in standardteckensnittsersättningen till "Courier New".
default_font_substitution_rule.default_font_name = 'Courier New'
# Med en dokumentbyggare, lägg till lite text i ett teckensnitt som vi inte har för att se substitutionen ske,
# och rendera sedan resultatet i en PDF.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Missing Font'
builder.writeln('Line written in a missing font, which will be substituted with Courier New.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontSubstitutionRule.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSubstitutionSettings](../)

