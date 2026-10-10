---
title: LoadOptions.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "LoadOptions.font_settings property. Allows to specify document font settings."
type: docs
weight: 60
url: /sv/python-net/aspose.words.loading/loadoptions/font_settings/
---

## LoadOptions.font_settings property

Allows to specify document font settings.


```python
@property
def font_settings(self) -> aspose.words.fonts.FontSettings:
    ...

@font_settings.setter
def font_settings(self, value: aspose.words.fonts.FontSettings):
    ...

```

### Remarks

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words
may resolve the fonts to perform font fallback.

If set to ``None``, default static font settings [FontSettings.default_instance](../../../aspose.words.fonts/fontsettings/default_instance/) will be used.

The default value is ``None``.




### Examples

Shows how to designate font substitutes during loading.

```python
load_options = aw.loading.LoadOptions()
load_options.font_settings = aw.fonts.FontSettings()
# Ställ in en teckensnittssubstitutionsregel för ett LoadOptions‑objekt.
# Om dokumentet vi laddar använder ett teckensnitt som vi inte har,
# kommer den här regeln att ersätta det otillgängliga teckensnittet med ett som finns.
# I detta fall kommer alla förekomster av \"MissingFont\" att konverteras till \"Comic Sans MS\".
substitution_rule = load_options.font_settings.substitution_settings.table_substitution
substitution_rule.add_substitutes('MissingFont', ['Comic Sans MS'])
doc = aw.Document(file_name=MY_DIR + 'Missing font.html', load_options=load_options)
# Vid denna tidpunkt kommer sådan text fortfarande att vara i \"MissingFont\".
# Teckensnittssubstitution kommer att ske när vi renderar dokumentet.
self.assertEqual('MissingFont', doc.first_section.body.first_paragraph.runs[0].font.name)
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.ResolveFontsBeforeLoadingDocument.pdf')
```

Shows how to apply font substitution settings while loading a document.

```python
# Skapa ett FontSettings‑objekt som kommer att ersätta teckensnittet \"Times New Roman\"
# med teckensnittet \"Arvo\" från vår \"MyFonts\"‑mapp.
font_settings = aw.fonts.FontSettings()
font_settings.set_fonts_folder(FONTS_DIR, False)
font_settings.substitution_settings.table_substitution.add_substitutes('Times New Roman', ['Arvo'])
# Ställ in det FontSettings‑objektet som en egenskap för ett nyss skapat LoadOptions‑objekt.
load_options = aw.loading.LoadOptions()
load_options.font_settings = font_settings
# Läs in dokumentet, rendera det sedan som en PDF med teckensnittssubstitutionen.
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'LoadOptions.FontSettings.pdf')
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

