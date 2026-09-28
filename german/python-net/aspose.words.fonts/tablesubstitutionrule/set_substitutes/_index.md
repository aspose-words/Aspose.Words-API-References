---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /de/python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
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
# Die standardmäßigen Schriftquellen enthalten die erste Schrift, die das Dokument verwendet.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# Die zweite Schrift, "Amethysta", ist nicht verfügbar.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Wir können eine Schrift-Ersetzungstabelle konfigurieren, die bestimmt
# welche Schriften Aspose.Words als Ersatz für nicht verfügbare Schriften verwendet.
# Legen Sie zwei Ersatzschriften für "Amethysta" fest: "Arvo" und "Courier New".
# Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words den zweiten Ersatz zu verwenden, und so weiter.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" ist nicht verfügbar, und die Ersetzungsregel besagt, dass die erste zu verwendende Ersatzschrift "Arvo" ist.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" ist ebenfalls nicht verfügbar, aber "Courier New" ist es.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Das Ausgabedokument zeigt den Text, der die Schrift "Amethysta" verwendet, formatiert mit "Courier New".
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

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
* class [TableSubstitutionRule](../)

