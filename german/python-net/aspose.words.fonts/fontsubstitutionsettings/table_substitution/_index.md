---
title: FontSubstitutionSettings.table_substitution property
linktitle: table_substitution property
articleTitle: table_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.table_substitution property. Settings related to table substitution rule."
type: docs
weight: 50
url: /de/python-net/aspose.words.fonts/fontsubstitutionsettings/table_substitution/
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
# Erstellen Sie eine neue Tabellen-Substitutionsregel und laden Sie die standardmäßige Windows-Schriftart-Substitutionstabelle.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Wenn wir Schriftarten ausschließlich aus unserem Ordner auswählen, benötigen wir eine benutzerdefinierte Substitutionstabelle.
# Wir haben keinen Zugriff mehr auf die Microsoft Windows-Schriftarten,
# wie "Arial" oder "Times New Roman", da sie in unserem neuen Schriftartenordner nicht existieren.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# Unten sind zwei Methoden zum Laden einer Substitutionstabelle aus einer Datei im lokalen Dateisystem aufgeführt.
# 1 -  Aus einem Stream:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Direkt aus einer Datei:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Da wir keinen Zugriff mehr auf "Arial" haben, wird unsere Schriftarttabelle zunächst versuchen, sie durch "Nonexistent Font" zu ersetzen.
# Wir besitzen diese Schriftart nicht, sodass sie zur nächsten Alternative, "Kreon", im Ordner "MyFonts", übergeht.
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Wir können diese Tabelle programmgesteuert erweitern. Wir werden einen Eintrag hinzufügen, der "Times New Roman" durch "Arvo" ersetzt.
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Wir können mit AddSubstitutes() einen sekundären Fallback-Ersatz für einen vorhandenen Schriftarteintrag hinzufügen.
# Falls "Arvo" nicht verfügbar ist, sucht unsere Tabelle nach "M+ 2m" als zweite Ersatzoption.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() kann eine neue Liste von Ersatzschriften für eine Schrift festlegen.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Das Schreiben von Text in Schriften, auf die wir keinen Zugriff haben, löst unsere Ersetzungsregeln aus.
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

