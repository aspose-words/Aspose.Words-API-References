---
title: FontSubstitutionSettings.table_substitution property
linktitle: table_substitution property
articleTitle: table_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.table_substitution property. Settings related to table substitution rule."
type: docs
weight: 50
url: /fr/python-net/aspose.words.fonts/fontsubstitutionsettings/table_substitution/
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
# Créez une nouvelle règle de substitution de table et chargez la table de substitution de polices Windows par défaut.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Si nous sélectionnons les polices exclusivement depuis notre dossier, nous aurons besoin d'une table de substitution personnalisée.
# Nous n'aurons plus accès aux polices Microsoft Windows,
# telles que "Arial" ou "Times New Roman" car elles n'existent pas dans notre nouveau dossier de polices.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# Voici deux manières de charger une table de substitution à partir d'un fichier du système de fichiers local.
# 1 -  À partir d'un flux:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Directement depuis un fichier:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Puisque nous n'avons plus accès à "Arial", notre table de polices essaiera d'abord de la substituer par "Nonexistent Font".
# Nous ne disposons pas de cette police, elle passera donc à la substitution suivante, "Kreon", trouvée dans le dossier "MyFonts".
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Nous pouvons étendre cette table de manière programmatique. Nous ajouterons une entrée qui substitue "Times New Roman" par "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Nous pouvons ajouter un substitut de secours secondaire pour une entrée de police existante avec AddSubstitutes().
# Dans le cas où "Arvo" n'est pas disponible, notre tableau recherchera "M+ 2m" comme deuxième option de substitution.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() peut définir une nouvelle liste de polices de substitution pour une police.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Écrire du texte avec des polices auxquelles nous n'avons pas accès déclenchera nos règles de substitution.
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

