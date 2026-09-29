---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /sv/python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
---

## set_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Override substitute font names for given original font name.


```python
def set_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |
| substitute_font_names | List[str] | List of alternative font names. |

### Examples

Shows how set font substitution rules.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Standardkällorna för teckensnitt innehåller det första teckensnittet som dokumentet använder.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# Det andra teckensnittet, \"Amethysta\", är inte tillgängligt.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Vi kan konfigurera en teckensnittssubstitutionstabell som bestämmer
# vilka teckensnitt Aspose.Words kommer att använda som substitut för otillgängliga teckensnitt.
# Ange två substitutteckensnitt för \"Amethysta\": \"Arvo\" och \"Courier New\".
# Om det första substitutet inte är tillgängligt, försöker Aspose.Words använda det andra substitutet, och så vidare.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# \"Amethysta\" är inte tillgängligt, och substitutionsregeln anger att det första teckensnittet att använda som substitut är \"Arvo\".
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# \"Arvo\" är också otillgängligt, men \"Courier New\" är det.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Utdokumentet kommer att visa texten som använder teckensnittet \"Amethysta\" formaterat med \"Courier New\".
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

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
* class [TableSubstitutionRule](../)

