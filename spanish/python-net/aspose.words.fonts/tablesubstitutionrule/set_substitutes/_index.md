---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /es/python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
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
# Las fuentes predeterminadas contienen la primera fuente que usa el documento.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# La segunda fuente, "Amethysta", no está disponible.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Podemos configurar una tabla de sustitución de fuentes que determina
# qué fuentes usará Aspose.Words como sustitutos de fuentes no disponibles.
# Establezca dos fuentes de sustitución para "Amethysta": "Arvo" y "Courier New".
# Si el primer sustituto no está disponible, Aspose.Words intentará usar el segundo sustituto, y así sucesivamente.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" no está disponible, y la regla de sustitución indica que la primera fuente a usar como sustituto es "Arvo".
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" también está indisponible, pero "Courier New" sí lo está.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# El documento de salida mostrará el texto que usa la fuente "Amethysta" formateado con "Courier New".
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

Shows how to work with custom font substitution tables.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# Crea una nueva regla de sustitución de tabla y carga la tabla de sustitución de fuentes predeterminada de Windows.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Si seleccionamos fuentes exclusivamente de nuestra carpeta, necesitaremos una tabla de sustitución personalizada.
# Ya no tendremos acceso a las fuentes de Microsoft Windows,
# como "Arial" o "Times New Roman" ya que no existen en nuestra nueva carpeta de fuentes.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# A continuación se presentan dos formas de cargar una tabla de sustitución desde un archivo en el sistema de archivos local.
# 1 -  Desde un flujo:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Directamente desde un archivo:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Dado que ya no tenemos acceso a "Arial", nuestra tabla de fuentes intentará primero sustituirla con "Nonexistent Font".
# No disponemos de esta fuente, por lo que pasará a la siguiente sustituta, "Kreon", encontrada en la carpeta "MyFonts".
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Podemos expandir esta tabla programáticamente. Añadiremos una entrada que sustituya "Times New Roman" con "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Podemos agregar un sustituto de reserva secundario para una entrada de fuente existente con AddSubstitutes().
# En caso de que "Arvo" no esté disponible, nuestra tabla buscará "M+ 2m" como segunda opción de sustituto.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() puede establecer una nueva lista de fuentes sustitutas para una fuente.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Escribir texto con fuentes a las que no tenemos acceso activará nuestras reglas de sustitución.
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

