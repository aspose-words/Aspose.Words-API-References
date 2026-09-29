---
title: TableSubstitutionRule.add_substitutes method
linktitle: add_substitutes method
articleTitle: add_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.add_substitutes method. Adds substitute font names for given original font name."
type: docs
weight: 10
url: /sv/python-net/aspose.words.fonts/tablesubstitutionrule/add_substitutes/
---

## add_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Adds substitute font names for given original font name.


```python
def add_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |
| substitute_font_names | List[str] | List of alternative font names. |

### Examples

Shows how to access a document's system font source and set font substitutes.

```python
import platform
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR

class TestFontSubstitution(ApiExampleBase):

    def test_font_substitution(self):
        doc = aw.Document()
        doc.font_settings = aw.fonts.FontSettings()
        # Som standard innehåller ett tomt dokument alltid en systemteckensnittskälla.
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        system_font_source = doc.font_settings.get_fonts_sources()[0].as_system_font_source()
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, system_font_source.type)
        self.assertEqual(0, system_font_source.priority)
        is_windows = platform.system() == 'Windows'
        if is_windows:
            fonts_path = 'C:\\WINDOWS\\Fonts'
            actual = None
            cond_expression = next(iter(aw.fonts.SystemFontSource.get_system_font_folders()), None)
            if cond_expression is not None:
                actual = cond_expression.lower()
            self.assertEqual(fonts_path.lower(), actual)
        for system_font_folder in aw.fonts.SystemFontSource.get_system_font_folders():
            print(system_font_folder)
        # Ange ett teckensnitt som finns i Windows Fonts-katalogen som en ersättning för ett som inte finns.
        doc.font_settings.substitution_settings.font_info_substitution.enabled = True
        doc.font_settings.substitution_settings.table_substitution.add_substitutes('Kreon-Regular', ['Calibri'])
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertIn('Calibri', doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular'))
        # Alternativt kan vi lägga till en mappteckensnittskälla där den motsvarande mappen innehåller teckensnittet.
        folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
        doc.font_settings.set_fonts_sources(sources=[system_font_source, folder_font_source])
        self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))
        # Att återställa teckensnittskällorna lämnar oss fortfarande med systemteckensnittskällan samt våra ersättningar.
        doc.font_settings.reset_font_sources()
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, doc.font_settings.get_fonts_sources()[0].type)
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertTrue(doc.font_settings.substitution_settings.font_name_substitution.enabled)
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

