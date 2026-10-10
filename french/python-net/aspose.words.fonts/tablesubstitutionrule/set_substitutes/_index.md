---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /fr/python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
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
# Les sources de polices par défaut contiennent la première police utilisée par le document.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# La deuxième police, "Amethysta", n'est pas disponible.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Nous pouvons configurer une table de substitution de polices qui détermine
# quelles polices Aspose.Words utilisera comme substituts pour les polices indisponibles.
# Définissez deux polices de substitution pour "Amethysta" : "Arvo" et "Courier New".
# Si le premier substitut n'est pas disponible, Aspose.Words tente d'utiliser le deuxième substitut, et ainsi de suite.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" n'est pas disponible, et la règle de substitution indique que la première police à utiliser comme substitut est "Arvo".
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" n'est également pas disponible, mais "Courier New" l'est.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Le document de sortie affichera le texte qui utilise la police "Amethysta" formatée avec "Courier New".
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

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
* class [TableSubstitutionRule](../)

