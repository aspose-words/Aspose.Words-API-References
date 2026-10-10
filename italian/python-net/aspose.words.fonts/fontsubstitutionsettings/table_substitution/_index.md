---
title: FontSubstitutionSettings.table_substitution property
linktitle: table_substitution property
articleTitle: table_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.table_substitution property. Settings related to table substitution rule."
type: docs
weight: 50
url: /it/python-net/aspose.words.fonts/fontsubstitutionsettings/table_substitution/
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
# Crea una nuova regola di sostituzione della tabella e carica la tabella di sostituzione dei font di Windows predefinita.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Se selezioniamo i font esclusivamente dalla nostra cartella, avremo bisogno di una tabella di sostituzione personalizzata.
# Non avremo più accesso ai font di Microsoft Windows,
# come "Arial" o "Times New Roman" poiché non esistono nella nostra nuova cartella dei font.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# Di seguito sono riportati due modi per caricare una tabella di sostituzione da un file nel file system locale.
# 1 -  Da uno stream:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Direttamente da un file:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Poiché non abbiamo più accesso a "Arial", la nostra tabella dei font proverà prima a sostituirlo con "Nonexistent Font".
# Non possediamo questo font, quindi passerà al successivo sostituto, "Kreon", trovato nella cartella "MyFonts".
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Possiamo espandere questa tabella programmaticamente. Aggiungeremo una voce che sostituisce "Times New Roman" con "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Possiamo aggiungere una sostituzione di fallback secondaria per una voce di carattere esistente con AddSubstitutes().
# Nel caso in cui "Arvo" non sia disponibile, la nostra tabella cercherà "M+ 2m" come seconda opzione di sostituzione.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() può impostare una nuova lista di caratteri sostitutivi per un carattere.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Scrivere testo con caratteri a cui non abbiamo accesso attiverà le nostre regole di sostituzione.
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

