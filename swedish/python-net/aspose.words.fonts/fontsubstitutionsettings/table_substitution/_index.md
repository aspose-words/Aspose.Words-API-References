---
title: FontSubstitutionSettings.table_substitution property
linktitle: table_substitution property
articleTitle: table_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.table_substitution property. Settings related to table substitution rule."
type: docs
weight: 50
url: /sv/python-net/aspose.words.fonts/fontsubstitutionsettings/table_substitution/
---

## FontSubstitutionSettings.table_substitution property

Settings related to table substitution rule.


```python
@property
def table_substitution(self) -> aspose.words.fonts.TableSubstitutionRule:
    ...

```

### Examples

Shows how to work with custom font substitution tables.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# Skapa en ny tabellsubstitutionsregel och läs in standardtabellen för Windows‑teckensnittssubstitution.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Om vi väljer teckensnitt uteslutande från vår mapp, kommer vi att behöva en anpassad substitutions‑tabell.
# Vi kommer inte längre att ha åtkomst till Microsoft Windows‑teckensnitten,
# såsom "Arial" eller "Times New Roman" eftersom de inte finns i vår nya teckensnittsmapp.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# Nedan finns två sätt att läsa in en substitutions‑tabell från en fil i det lokala filsystemet.
# 1 -  Från en ström:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Direkt från en fil:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Eftersom vi inte längre har åtkomst till "Arial" kommer vår teckensnittstabell först att försöka ersätta den med "Nonexistent Font".
# Vi har inte detta teckensnitt så den kommer att gå vidare till nästa ersättning, "Kreon", som finns i mappen "MyFonts".
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Vi kan expandera den här tabellen programmässigt. Vi kommer att lägga till en post som ersätter "Times New Roman" med "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Vi kan lägga till en sekundär reservsubstitution för en befintlig teckensnittspost med AddSubstitutes().
# Om \"Arvo\" inte är tillgängligt, kommer vår tabell att leta efter \"M+ 2m\" som ett andra substitutionsalternativ.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() kan ange en ny lista med substitutteckensnitt för ett teckensnitt.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Att skriva text i teckensnitt som vi inte har åtkomst till kommer att aktivera våra substitutionsregler.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Text written in Arial, to be substituted by Kreon.')
builder.font.name = 'Times New Roman'
builder.writeln('Text written in Times New Roman, to be substituted by Squarish Sans CT.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Custom.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSubstitutionSettings](../)

